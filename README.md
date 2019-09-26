# Connected-and-automated-vehicle-simulation-platform
%This software is developed based on matlab2018a and is mainly based on cellular automata theory for discrete simulation.



function varargout = GUI_1(varargin)
% GUI_1 MATLAB code for GUI_1.fig
%      GUI_1, by itself, creates a new GUI_1 or raises the existing
%      singleton*.
%
%      H = GUI_1 returns the handle to a new GUI_1 or the handle to
%      the existing singleton*.
%
%      GUI_1('CALLBACK',hObject,eventData,handles,...) calls the local
%      function named CALLBACK in GUI_1.M with the given input arguments.
%
%      GUI_1('Property','Value',...) creates a new GUI_1 or raises the
%      existing singleton*.  Starting from the left, property value pairs are
%      applied to the GUI before GUI_1_OpeningFcn gets called.  An
%      unrecognized property name or invalid value makes property application
%      stop.  All inputs are passed to GUI_1_OpeningFcn via varargin.
%
%      *See GUI Options on GUIDE's Tools menu.  Choose "GUI allows only one
%      instance to run (singleton)".
%
% See also: GUIDE, GUIDATA, GUIHANDLES

% Edit the above text to modify the response to help GUI_1

% Last Modified by GUIDE v2.5 24-Sep-2019 21:03:42

% Begin initialization code - DO NOT EDIT
gui_Singleton = 1;
gui_State = struct('gui_Name',       mfilename, ...
                   'gui_Singleton',  gui_Singleton, ...
                   'gui_OpeningFcn', @GUI_1_OpeningFcn, ...
                   'gui_OutputFcn',  @GUI_1_OutputFcn, ...
                   'gui_LayoutFcn',  [] , ...
                   'gui_Callback',   []);
if nargin && ischar(varargin{1})
    gui_State.gui_Callback = str2func(varargin{1});
end

if nargout
    [varargout{1:nargout}] = gui_mainfcn(gui_State, varargin{:});
else
    gui_mainfcn(gui_State, varargin{:});
end
% End initialization code - DO NOT EDIT


% --- Executes just before GUI_1 is made visible.
function GUI_1_OpeningFcn(hObject, eventdata, handles, varargin)
% This function has no output args, see OutputFcn.
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
% varargin   command line arguments to GUI_1 (see VARARGIN)
Games.ax = axes('units','normalized', 'position',[0 0 1 1]); %单位化
uistack(Games.ax,'down');   %把新创建的坐标系在下移一层
% Path=which('test');
% Path=[pwd,'\封面.m'];
Games.img = imread('title1.jpg'); %打开图片
Games.IH = image(Games.img); % 显示图片
colormap gray % 设置窗口的调色板为灰色
set(Games.ax,'handlevisibility','off','visible','off');%把创建的坐标系句柄设为不可见

Games2.ax=axes('units','normalized','pos',[0 0 1 1]); 
text(0.15,0.85,'自动驾驶微观交通仿真平台试用版 1.1','fontsize',30,'FontWeight','bold') %第一个数横坐标，第二个数纵坐标
% text(0.5,0.8,'请任选一项，开始你的表演！','fontsize',40,'color','b') 
% text(0.1,0.4,'参 数 选 定','FontName','微软雅黑','fontsize',25,'color','w')
% text(0.1,0.2,'查 看 结 果','FontName','微软雅黑','fontsize',25,'color','w')
% text(0.7,0.4,'启 动 程 序','FontName','微软雅黑','fontsize',25,'color','w')
% text(0.7,0.2,'联 系 我 们','FontName','微软雅黑','fontsize',25,'color','w')
text(0.77,0.05,'220183023@seu.edu.cn','fontsize',12)
set(Games2.ax,'handlevisibility','off','visible','off');

% Choose default command line output for GUI_1
handles.output = hObject;

% Update handles structure
guidata(hObject, handles);

% UIWAIT makes GUI_1 wait for user response (see UIRESUME)
% uiwait(handles.gui1);


% --- Outputs from this function are returned to the command line.
function varargout = GUI_1_OutputFcn(hObject, eventdata, handles) 
% varargout  cell array for returning output args (see VARARGOUT);
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get default command line output from handles structure
varargout{1} = handles.output;


% --- Executes on button press in pushbutton1.
function pushbutton1_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton1 (see GCBO)4
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)


% --- Executes on button press in canshuxuanding.
function canshuxuanding_Callback(hObject, eventdata, handles)
% hObject    handle to canshuxuanding (see GCBO)
% set(handles.figure1,'visible','off');
close('GUI_1');
run('GUI_canshuxuanding');

% figure;
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)


% --- Executes on button press in pushbutton4.
function pushbutton4_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton4 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA) f         
close('GUI_1');
run('chakanjieguo');

% --- Executes on button press in pushbutton5.
function pushbutton5_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton5 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
close('GUI_1');
run('GUI_contact');

% --- Executes on button press in pushbutton6.
function pushbutton6_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton6 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
url = 'https://docs.qq.com/doc/DVHVSVWN3ZmNacFRR';
web(url,'-browser')
