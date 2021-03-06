---
order: 0
title: Classic
---

典型结果页面。

```ts
import { Component } from '@angular/core';

@Component({
    selector: 'app-demo',
    template: `
<result
    type="success"
    [title]="'提交成功'"
    description="提交结果页用于反馈一系列操作任务的处理结果，如果仅是简单操作，使用 Message 全局提示反馈即可。本文字区域可以展示简单的补充说明，如果有类似展示x“单据”的需求，下面这个灰色区域可以呈现比较复杂的内容。"
    [extra]="resultExtra">
    <ng-template #resultExtra>
        <nz-steps [nzCurrent]="1">
            <nz-step [nzTitle]="'创建项目'" [nzDescription]="createDesc">
                <ng-template #createDesc>
                    <p class="my-sm">曲丽丽<nz-icon nzType="dingding-o" class="ml-sm"></nz-icon></p>
                    <p>2016-12-12 12:32</p>
                </ng-template>
            </nz-step>
            <nz-step [nzTitle]="'部门初审'" [nzDescription]="checkedDesc">
                <ng-template #checkedDesc>
                    <p class="my-sm">周毛毛<nz-icon nzType="dingding-o" style="color: #00A0E9" class="ml-sm"></nz-icon></p>
                    <a (click)="msg.success('click')">催一下</a>
                </ng-template>
            </nz-step>
            <nz-step [nzTitle]="'财务复核'"></nz-step>
            <nz-step [nzTitle]="'完成'"></nz-step>
        </nz-steps>
    </ng-template>
    <button nz-button [nzType]="'primary'" [nzSize]="'large'">返回列表</button>
    <button nz-button [nzSize]="'large'">查看项目</button>
    <button nz-button [nzSize]="'large'">打 印</button>
</result>
    `
})
export class DemoComponent {
}
```
