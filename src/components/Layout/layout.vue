<template>
    <div class="layout app-container">
        <div class="layout-header">
            <div class="layout-header-system-name">
                乐课力财务中台
            </div>

            <div class="layout-header-actions">

            </div>
        </div>

        <div class="layout-menus">

        </div>

        <div class="layout-content">
            <slot />
        </div>
    </div>
</template>

<style scoped lang="scss">
.layout {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    flex-direction: column;
    flex-wrap: wrap;
    background-color: #f2f3f4;
    padding-top: 60px;
    padding-left: 220px;
    .layout-header {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 9;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 var(--root-padding-default);
        box-sizing: border-box;
        width: 100%;
        height: 60px;
        background-color: #fff;
        box-shadow: var(--root-shadow);
        .layout-header-system-name {
            font-size: var(--root-font-size-super);
            letter-spacing: 2px;
        }
    }
    .layout-menus {
        position: fixed;
        top: 60px;
        left: 0;
        display: inline-flex;
        width: 220px;
        height: calc(100% - 60px);
        box-shadow: var(--root-shadow);
        background-color: #fff;
    }
    .layout-content {
        display: flex;
        width: calc(100% - 220px);
        height: calc(100% - 60px);
        padding: var(--root-padding-default);
        box-sizing: border-box;
    }
}
</style>