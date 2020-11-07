---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: ba1c4c8267089d71a265de07b0f9508a24cf9b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751201"
---
# <span data-ttu-id="9f70a-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f70a-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="9f70a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f70a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f70a-103">Analysis Services sunucusu örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="9f70a-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="9f70a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f70a-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f70a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f70a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f70a-106">Resume-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="9f70a-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="9f70a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f70a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f70a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f70a-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="9f70a-109">Bu komut, resourcegroup testgroup 'da TestServer adlı duraklatılmış bir sunucuyu sürdürecek</span><span class="sxs-lookup"><span data-stu-id="9f70a-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="9f70a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f70a-110">PARAMETERS</span></span>

### <span data-ttu-id="9f70a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f70a-111">-DefaultProfile</span></span>
<span data-ttu-id="9f70a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f70a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f70a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f70a-113">-Name</span></span>
<span data-ttu-id="9f70a-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="9f70a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9f70a-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9f70a-115">-PassThru</span></span>
<span data-ttu-id="9f70a-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="9f70a-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="9f70a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f70a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f70a-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9f70a-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9f70a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f70a-119">-Confirm</span></span>
<span data-ttu-id="9f70a-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="9f70a-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9f70a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f70a-121">-WhatIf</span></span>
<span data-ttu-id="9f70a-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="9f70a-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9f70a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f70a-123">CommonParameters</span></span>
<span data-ttu-id="9f70a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f70a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f70a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f70a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f70a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f70a-126">INPUTS</span></span>

### <span data-ttu-id="9f70a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9f70a-127">System.String</span></span>

## <span data-ttu-id="9f70a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f70a-128">OUTPUTS</span></span>

### <span data-ttu-id="9f70a-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f70a-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9f70a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f70a-130">NOTES</span></span>
<span data-ttu-id="9f70a-131">Diğer ad: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="9f70a-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="9f70a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f70a-132">RELATED LINKS</span></span>

[<span data-ttu-id="9f70a-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f70a-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="9f70a-134">Askıya al-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f70a-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
