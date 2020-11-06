---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588916"
---
# <span data-ttu-id="06909-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="06909-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="06909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06909-102">SYNOPSIS</span></span>
<span data-ttu-id="06909-103">Günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06909-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06909-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06909-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06909-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06909-105">DESCRIPTION</span></span>
<span data-ttu-id="06909-106">**Remove-AzureRmLogProfile** cmdlet 'i, günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06909-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="06909-107">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="06909-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="06909-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06909-108">EXAMPLES</span></span>

## <span data-ttu-id="06909-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06909-109">PARAMETERS</span></span>

### <span data-ttu-id="06909-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06909-110">-DefaultProfile</span></span>
<span data-ttu-id="06909-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="06909-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06909-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="06909-112">-Name</span></span>
<span data-ttu-id="06909-113">Kaldırılacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06909-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="06909-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="06909-114">-PassThru</span></span>
<span data-ttu-id="06909-115">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="06909-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="06909-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06909-116">CommonParameters</span></span>
<span data-ttu-id="06909-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06909-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06909-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06909-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06909-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06909-119">INPUTS</span></span>

### <span data-ttu-id="06909-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="06909-120">None</span></span>
<span data-ttu-id="06909-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="06909-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06909-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06909-122">OUTPUTS</span></span>

### <span data-ttu-id="06909-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="06909-123">AzureOperationResponse</span></span>

## <span data-ttu-id="06909-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06909-124">NOTES</span></span>

## <span data-ttu-id="06909-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06909-125">RELATED LINKS</span></span>

[<span data-ttu-id="06909-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="06909-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="06909-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="06909-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


