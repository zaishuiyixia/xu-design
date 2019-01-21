<template>
    <button class="g-button" :class="{[`icon-${iconPosition}`]: true}">
        <g-icon v-if="icon" class="icon" :name="icon"></g-icon>
        <g-icon class="loading" name="loading"></g-icon>
        <div class="content">
            <slot></slot>
        </div>
    </button>
</template>
<script>
    export default {
        // props: ['icon', 'iconPosition']
        props: {
            icon: {},
            iconPosition: {
                type: String,
                default: 'left',
                validator: function (value) {
                    return value === 'left' || value === 'right'
                }
            }
        }
    }
</script>
<style lang="scss">
    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
    .loading {
        animation: spin 2s infinite linear;
    }
    .g-button {
        font-size: var(--font-size); height: var(--button-height);padding: 0 1em; /* 按钮左右空出来一个字的大小。给按钮写死宽高是不太好的选择 */
        border-radius: var(--border-radius); border: 1px solid var(--border-color);
        background: var(--button-bg);
        display: inline-flex; justify-content: center; align-items: center;
        vertical-align: middle;
        &:hover { border-color: var(--border-color-hover); }
        &:active { border-color: var(--button-active-bg); }
        &:focus { outline: none; }
        > .icon { order: 1; margin-right: .5em; }
        > .content { order: 2; }
        &.icon-right {
            > .icon { order: 2; margin-right: 0em; margin-left: .5em; }
            > .content { order: 1; }
        }
    }
</style>