---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587050"
---
# <span data-ttu-id="b8e66-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8e66-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b8e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e66-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e66-103">Analysis Services sunucusu örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="b8e66-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8e66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8e66-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8e66-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e66-106">Suspend-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="b8e66-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="b8e66-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8e66-107">EXAMPLES</span></span>

### <span data-ttu-id="b8e66-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8e66-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="b8e66-109">Bu komut, resourcegroup test grubunda TestServer adlı etkin bir sunucuyu askıya alacaktır</span><span class="sxs-lookup"><span data-stu-id="b8e66-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="b8e66-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8e66-110">PARAMETERS</span></span>

### <span data-ttu-id="b8e66-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8e66-111">-Name</span></span>
<span data-ttu-id="b8e66-112">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="b8e66-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b8e66-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b8e66-113">-PassThru</span></span>
<span data-ttu-id="b8e66-114">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="b8e66-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="b8e66-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e66-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8e66-116">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b8e66-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="b8e66-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8e66-117">-Confirm</span></span>
<span data-ttu-id="b8e66-118">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="b8e66-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="b8e66-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e66-119">-WhatIf</span></span>
<span data-ttu-id="b8e66-120">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="b8e66-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="b8e66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e66-121">CommonParameters</span></span>
<span data-ttu-id="b8e66-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8e66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e66-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e66-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e66-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8e66-124">INPUTS</span></span>

## <span data-ttu-id="b8e66-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8e66-125">OUTPUTS</span></span>

### <span data-ttu-id="b8e66-126">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8e66-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="b8e66-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8e66-127">NOTES</span></span>
<span data-ttu-id="b8e66-128">Diğer ad: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b8e66-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="b8e66-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8e66-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8e66-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8e66-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="b8e66-131">Özgeçmiş-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8e66-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

