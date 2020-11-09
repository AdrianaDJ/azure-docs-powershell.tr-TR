---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321925"
---
# <span data-ttu-id="f4ad8-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f4ad8-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="f4ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ad8-103">Ağ geçidine gelen/giden HTTP iletileri için Tanılama ayarları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="f4ad8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4ad8-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4ad8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ad8-106">**New-Azapsananagementbir ardışık düzen ayarı** cmdlet 'i gelen/giden http Iletileri için tanılama ayarlarını ağ geçidine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="f4ad8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4ad8-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ad8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4ad8-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="f4ad8-109">Tanılama varlığında ön uç veya arka uçta kullanılacak bir ardışık düzen tanılaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="f4ad8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4ad8-110">PARAMETERS</span></span>

### <span data-ttu-id="f4ad8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ad8-111">-DefaultProfile</span></span>
<span data-ttu-id="f4ad8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad8-113">-İstek</span><span class="sxs-lookup"><span data-stu-id="f4ad8-113">-Request</span></span>
<span data-ttu-id="f4ad8-114">Isteğin tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="f4ad8-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad8-116">-Response</span><span class="sxs-lookup"><span data-stu-id="f4ad8-116">-Response</span></span>
<span data-ttu-id="f4ad8-117">Yanıt için tanılama ayarı.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="f4ad8-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ad8-119">CommonParameters</span></span>
<span data-ttu-id="f4ad8-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ad8-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4ad8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ad8-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4ad8-122">INPUTS</span></span>

### <span data-ttu-id="f4ad8-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f4ad8-123">None</span></span>

## <span data-ttu-id="f4ad8-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4ad8-124">OUTPUTS</span></span>

### <span data-ttu-id="f4ad8-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementıngesinedınoçıkartma ayarı</span><span class="sxs-lookup"><span data-stu-id="f4ad8-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="f4ad8-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4ad8-126">NOTES</span></span>

## <span data-ttu-id="f4ad8-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4ad8-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4ad8-128">Get-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="f4ad8-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="f4ad8-129">Remove-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="f4ad8-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="f4ad8-130">Set-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="f4ad8-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="f4ad8-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f4ad8-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


