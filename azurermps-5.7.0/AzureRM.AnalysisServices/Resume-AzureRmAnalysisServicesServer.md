---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763289"
---
# <span data-ttu-id="59edb-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="59edb-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="59edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59edb-102">SYNOPSIS</span></span>
<span data-ttu-id="59edb-103">Analysis Services sunucusu örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="59edb-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59edb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59edb-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59edb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59edb-105">DESCRIPTION</span></span>
<span data-ttu-id="59edb-106">Resume-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini sürdürür</span><span class="sxs-lookup"><span data-stu-id="59edb-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="59edb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59edb-107">EXAMPLES</span></span>

### <span data-ttu-id="59edb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59edb-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="59edb-109">Bu komut, resourcegroup testgroup 'da TestServer adlı duraklatılmış bir sunucuyu sürdürecek</span><span class="sxs-lookup"><span data-stu-id="59edb-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="59edb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59edb-110">PARAMETERS</span></span>

### <span data-ttu-id="59edb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59edb-111">-DefaultProfile</span></span>
<span data-ttu-id="59edb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59edb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="59edb-113">-Name</span></span>
<span data-ttu-id="59edb-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="59edb-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59edb-115">-PassThru</span></span>
<span data-ttu-id="59edb-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="59edb-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59edb-117">-ResourceGroupName</span></span>
<span data-ttu-id="59edb-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="59edb-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="59edb-119">-Confirm</span></span>
<span data-ttu-id="59edb-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="59edb-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59edb-121">-WhatIf</span></span>
<span data-ttu-id="59edb-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="59edb-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59edb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59edb-123">CommonParameters</span></span>
<span data-ttu-id="59edb-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59edb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59edb-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59edb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59edb-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59edb-126">INPUTS</span></span>

### <span data-ttu-id="59edb-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59edb-127">None</span></span>
<span data-ttu-id="59edb-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59edb-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59edb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59edb-129">OUTPUTS</span></span>

### <span data-ttu-id="59edb-130">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="59edb-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="59edb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59edb-131">NOTES</span></span>
<span data-ttu-id="59edb-132">Diğer ad: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="59edb-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="59edb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59edb-133">RELATED LINKS</span></span>

[<span data-ttu-id="59edb-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="59edb-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="59edb-135">Askıya al-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="59edb-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
