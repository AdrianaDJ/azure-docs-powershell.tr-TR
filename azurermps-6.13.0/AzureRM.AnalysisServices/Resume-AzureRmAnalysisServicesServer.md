---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 28a89c40fcfd470d20d9b4423d40c38b43624edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762129"
---
# <span data-ttu-id="d37e2-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d37e2-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="d37e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e2-103">Analysis Services sunucusu örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="d37e2-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d37e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d37e2-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d37e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d37e2-106">Resume-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="d37e2-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d37e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d37e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d37e2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d37e2-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d37e2-109">Bu komut, resourcegroup testgroup 'da TestServer adlı duraklatılmış bir sunucuyu sürdürecek</span><span class="sxs-lookup"><span data-stu-id="d37e2-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d37e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d37e2-110">PARAMETERS</span></span>

### <span data-ttu-id="d37e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e2-111">-DefaultProfile</span></span>
<span data-ttu-id="d37e2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d37e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37e2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d37e2-113">-Name</span></span>
<span data-ttu-id="d37e2-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="d37e2-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d37e2-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d37e2-115">-PassThru</span></span>
<span data-ttu-id="d37e2-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="d37e2-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d37e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d37e2-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d37e2-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d37e2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d37e2-119">-Confirm</span></span>
<span data-ttu-id="d37e2-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="d37e2-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d37e2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37e2-121">-WhatIf</span></span>
<span data-ttu-id="d37e2-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="d37e2-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d37e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e2-123">CommonParameters</span></span>
<span data-ttu-id="d37e2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d37e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d37e2-126">INPUTS</span></span>

### <span data-ttu-id="d37e2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d37e2-127">System.String</span></span>

## <span data-ttu-id="d37e2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d37e2-128">OUTPUTS</span></span>

### <span data-ttu-id="d37e2-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d37e2-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d37e2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d37e2-130">NOTES</span></span>
<span data-ttu-id="d37e2-131">Diğer ad: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="d37e2-131">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="d37e2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d37e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="d37e2-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d37e2-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="d37e2-134">Askıya al-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d37e2-134">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
