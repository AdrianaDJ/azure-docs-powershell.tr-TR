---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763517"
---
# <span data-ttu-id="2678a-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2678a-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="2678a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2678a-102">SYNOPSIS</span></span>
<span data-ttu-id="2678a-103">Analysis Services sunucusu örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="2678a-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2678a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2678a-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2678a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2678a-105">DESCRIPTION</span></span>
<span data-ttu-id="2678a-106">Suspend-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="2678a-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="2678a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2678a-107">EXAMPLES</span></span>

### <span data-ttu-id="2678a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2678a-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2678a-109">Bu komut, resourcegroup test grubunda TestServer adlı etkin bir sunucuyu askıya alacaktır</span><span class="sxs-lookup"><span data-stu-id="2678a-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2678a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2678a-110">PARAMETERS</span></span>

### <span data-ttu-id="2678a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2678a-111">-DefaultProfile</span></span>
<span data-ttu-id="2678a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2678a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2678a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2678a-113">-Name</span></span>
<span data-ttu-id="2678a-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="2678a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2678a-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2678a-115">-PassThru</span></span>
<span data-ttu-id="2678a-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="2678a-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2678a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2678a-117">-ResourceGroupName</span></span>
<span data-ttu-id="2678a-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2678a-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2678a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2678a-119">-Confirm</span></span>
<span data-ttu-id="2678a-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="2678a-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2678a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2678a-121">-WhatIf</span></span>
<span data-ttu-id="2678a-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="2678a-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2678a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2678a-123">CommonParameters</span></span>
<span data-ttu-id="2678a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2678a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2678a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2678a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2678a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2678a-126">INPUTS</span></span>

### <span data-ttu-id="2678a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2678a-127">System.String</span></span>

## <span data-ttu-id="2678a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2678a-128">OUTPUTS</span></span>

### <span data-ttu-id="2678a-129">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2678a-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2678a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2678a-130">NOTES</span></span>
<span data-ttu-id="2678a-131">Diğer ad: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="2678a-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="2678a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2678a-132">RELATED LINKS</span></span>

[<span data-ttu-id="2678a-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2678a-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="2678a-134">Özgeçmiş-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2678a-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

