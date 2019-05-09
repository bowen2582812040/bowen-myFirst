<div class="panel panel-primary">
        <div class="panel-heading"><h1>学生信息管理</h1></div>
        <div class="form-inline" style="margin: 5px">
            <input type="text" class="form-control" ng-model="searchName" placeholder="请输入姓名搜索">
            <a href="javaScript:void(0)" class="btn btn-default btn-sm" ng-click="search()">搜索</a>
            <a href="javaScript:void(0)" class="btn btn-default btn-sm" ng-click="searchReset()">重置</a>
            <button class="btn btn-success btn-sm" value="新增" ng-click="moShow()">新增</button>
            <button class="btn btn-danger btn-sm" ng-click="delAllStudent()">批量删除</button>
        </div>
        <div>
            <table class="table table-bordered table-striped table-hover text-center">
                <tr>
                    <td width="80"><input type="checkbox" id="allCheckbox" ng-click="delSelectAll()">全选</td>
                    <td>姓名</td>
                    <td>性别</td>
                    <td>年龄</td>
                    <td>住址</td>
                    <td>班级</td>
                    <td>生日</td>
                    <td class="col-md-2">操作</td>
                </tr>
                <tr ng-repeat="stud in studList">
                    <td><input type="checkbox" class="checkboxs" ng-click="delSelect($event,stud.sid)"
                               value="{{stud.sid}}"></td>
                    <td>{{stud.sname}}</td>
                    <td>{{stud.sex}}</td>
                    <td>{{stud.age}}</td>
                    <td>{{stud.addr}}</td>
                    <td>{{stud.cname}}</td>
                    <td>{{stud.birth}}</td>
                    <td class="col-md-2">
                        <a href="" class="btn btn-primary btn-sm" ng-click="updStudent(stud)">修改</a>
                        <a href="" class="btn btn-danger btn-sm" ng-click="delStudent(stud.sid)">删除</a>
                    </td>
                </tr>
                <!--分页-->
                <tr>
                    <td colspan="8" style="padding: 0px">
                        <tm-pagination conf="paginationConf"></tm-pagination>
                    </td>
                </tr>
            </table>
            <div class="panel-heading text-right">泽林信息版权所有...</div>
        </div>
    </div>
</div>
