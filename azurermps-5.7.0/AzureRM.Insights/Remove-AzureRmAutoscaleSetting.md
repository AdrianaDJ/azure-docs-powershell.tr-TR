---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588924"
---
# <span data-ttu-id="6d149-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6d149-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="6d149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d149-102">SYNOPSIS</span></span>
<span data-ttu-id="6d149-103">Otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d149-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d149-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d149-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d149-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d149-105">DESCRIPTION</span></span>
<span data-ttu-id="6d149-106">**Remove-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d149-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="6d149-107">Ayarın adını ve atandığı kaynak grubunun adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d149-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="6d149-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="6d149-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6d149-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d149-109">EXAMPLES</span></span>

## <span data-ttu-id="6d149-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d149-110">PARAMETERS</span></span>

### <span data-ttu-id="6d149-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d149-111">-DefaultProfile</span></span>
<span data-ttu-id="6d149-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6d149-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d149-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d149-113">-Name</span></span>
<span data-ttu-id="6d149-114">Kaldırılacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d149-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d149-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d149-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d149-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d149-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d149-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d149-117">CommonParameters</span></span>
<span data-ttu-id="6d149-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d149-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d149-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d149-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d149-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d149-120">INPUTS</span></span>

### <span data-ttu-id="6d149-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d149-121">None</span></span>
<span data-ttu-id="6d149-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6d149-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d149-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d149-123">OUTPUTS</span></span>

### <span data-ttu-id="6d149-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6d149-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="6d149-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d149-125">NOTES</span></span>

## <span data-ttu-id="6d149-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d149-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d149-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6d149-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="6d149-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6d149-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


