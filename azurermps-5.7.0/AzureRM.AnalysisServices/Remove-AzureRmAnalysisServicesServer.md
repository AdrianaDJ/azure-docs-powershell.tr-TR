---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 541f1a2039f8c7b54a71798432a9f009d57144c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592522"
---
# <span data-ttu-id="7a701-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7a701-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="7a701-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a701-102">SYNOPSIS</span></span>
<span data-ttu-id="7a701-103">Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="7a701-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a701-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a701-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a701-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a701-105">DESCRIPTION</span></span>
<span data-ttu-id="7a701-106">Remove-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="7a701-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="7a701-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a701-107">EXAMPLES</span></span>

### <span data-ttu-id="7a701-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a701-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="7a701-109">Bu komut, resourcegroup testgroup 'da TestServer adlı sunucuyu kaldıracak</span><span class="sxs-lookup"><span data-stu-id="7a701-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="7a701-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a701-110">PARAMETERS</span></span>

### <span data-ttu-id="7a701-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a701-111">-DefaultProfile</span></span>
<span data-ttu-id="7a701-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a701-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a701-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a701-113">-Name</span></span>
<span data-ttu-id="7a701-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="7a701-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7a701-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7a701-115">-PassThru</span></span>
<span data-ttu-id="7a701-116">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="7a701-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="7a701-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a701-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a701-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7a701-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="7a701-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a701-119">-Confirm</span></span>
<span data-ttu-id="7a701-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="7a701-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7a701-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a701-121">-WhatIf</span></span>
<span data-ttu-id="7a701-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="7a701-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7a701-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a701-123">CommonParameters</span></span>
<span data-ttu-id="7a701-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a701-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a701-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a701-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a701-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a701-126">INPUTS</span></span>

### <span data-ttu-id="7a701-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7a701-127">None</span></span>
<span data-ttu-id="7a701-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7a701-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a701-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a701-129">OUTPUTS</span></span>

### <span data-ttu-id="7a701-130">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7a701-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7a701-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a701-131">NOTES</span></span>
<span data-ttu-id="7a701-132">Diğer ad: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="7a701-132">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="7a701-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a701-133">RELATED LINKS</span></span>

[<span data-ttu-id="7a701-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7a701-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="7a701-135">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7a701-135">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
