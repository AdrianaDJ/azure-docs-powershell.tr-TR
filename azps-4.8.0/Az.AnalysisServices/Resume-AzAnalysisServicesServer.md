---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268154"
---
# <span data-ttu-id="2bdba-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2bdba-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2bdba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bdba-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdba-103">Analysis Services sunucusu örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="2bdba-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2bdba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bdba-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bdba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bdba-105">DESCRIPTION</span></span>
<span data-ttu-id="2bdba-106">Resume-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="2bdba-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2bdba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bdba-107">EXAMPLES</span></span>

### <span data-ttu-id="2bdba-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2bdba-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2bdba-109">Bu komut, resourcegroup testgroup 'da TestServer adlı duraklatılmış bir sunucuyu sürdürecek</span><span class="sxs-lookup"><span data-stu-id="2bdba-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2bdba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bdba-110">PARAMETERS</span></span>

### <span data-ttu-id="2bdba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bdba-111">-DefaultProfile</span></span>
<span data-ttu-id="2bdba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bdba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bdba-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bdba-113">-Name</span></span>
<span data-ttu-id="2bdba-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="2bdba-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bdba-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2bdba-115">-PassThru</span></span>
<span data-ttu-id="2bdba-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="2bdba-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bdba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bdba-117">-ResourceGroupName</span></span>
<span data-ttu-id="2bdba-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2bdba-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bdba-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2bdba-119">-Confirm</span></span>
<span data-ttu-id="2bdba-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="2bdba-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bdba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bdba-121">-WhatIf</span></span>
<span data-ttu-id="2bdba-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="2bdba-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bdba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdba-123">CommonParameters</span></span>
<span data-ttu-id="2bdba-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bdba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdba-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bdba-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdba-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bdba-126">INPUTS</span></span>

### <span data-ttu-id="2bdba-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2bdba-127">System.String</span></span>

## <span data-ttu-id="2bdba-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bdba-128">OUTPUTS</span></span>

### <span data-ttu-id="2bdba-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2bdba-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2bdba-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bdba-130">NOTES</span></span>
<span data-ttu-id="2bdba-131">Diğer ad: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="2bdba-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="2bdba-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bdba-132">RELATED LINKS</span></span>

[<span data-ttu-id="2bdba-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2bdba-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2bdba-134">Askıya al-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2bdba-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
