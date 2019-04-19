<template>

    <div class="uk-section-primary tm-section-texture">

        <navbar class="uk-navbar-transparent"/>

        <div class="uk-section uk-flex uk-flex-middle uk-text-center" uk-height-viewport="offset-top: true">
            <div class="uk-width-1-1">
                <div class="uk-container">

                    <p class="uk-margin-large-bottom">
                        <canvas style="color: #fff" width="142" height="117" uk-svg src="./images/download.svg"></canvas>
                    </p>

                    <h1>感谢使用 UIkit ！</h1>

                    <p class="uk-margin-medium-bottom uk-text-large">请支持 UIkit 开源项目和 UIkit 中文网项目，在你的圈子里分享一下吧。<br class="uk-visible@s"> 你的支持是我们前进的动力</p>

                    <div class="uk-grid-medium uk-child-width-auto uk-flex-inline" uk-grid>
                        <div>
                            <a class="uk-button uk-button-primary tm-button-primary uk-button-large" href="#" target="_blank">
                                <span class="uk-margin-small-right" uk-icon="icon: twitter"></span>
                                <span class="uk-text-middle">Share on Twitter</span>
                            </a>
                        </div>
                        <div>
                            <a class="uk-button uk-button-primary tm-button-primary uk-button-large" href="#" target="_blank">
                                <span class="uk-margin-small-right" uk-icon="icon: facebook"></span>
                                <span class="uk-text-middle">Post on Facebook</span>
                            </a>
                        </div>
                    </div>

                </div>
            </div>
        </div>

    </div>

</template>

<script>

    import {ajax} from 'uikit-util';

    export default {

        mounted() {

            ajax('assets/uikit/package.json', {responseType: 'json'}).then(({response}) =>
                setTimeout(() => location.href = `https://github.com/uikit/uikit/releases/download/v${response.version}/uikit-${response.version}.zip`, 100)
            );

        }
    };

</script>
