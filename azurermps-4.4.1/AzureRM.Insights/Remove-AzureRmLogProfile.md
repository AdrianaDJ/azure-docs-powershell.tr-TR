---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763369"
---
# <span data-ttu-id="eb207-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb207-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="eb207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb207-102">SYNOPSIS</span></span>
<span data-ttu-id="eb207-103">Günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb207-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb207-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb207-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb207-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb207-105">DESCRIPTION</span></span>
<span data-ttu-id="eb207-106">**Remove-AzureRmLogProfile** cmdlet 'i, günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb207-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="eb207-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb207-107">EXAMPLES</span></span>

## <span data-ttu-id="eb207-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb207-108">PARAMETERS</span></span>

### <span data-ttu-id="eb207-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb207-109">-Name</span></span>
<span data-ttu-id="eb207-110">Kaldırılacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb207-110">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb207-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb207-111">-DefaultProfile</span></span>
<span data-ttu-id="eb207-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb207-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb207-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="eb207-113">-PassThru</span></span>
<span data-ttu-id="eb207-114">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="eb207-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eb207-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb207-115">CommonParameters</span></span>
<span data-ttu-id="eb207-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb207-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb207-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb207-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb207-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb207-118">INPUTS</span></span>

## <span data-ttu-id="eb207-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb207-119">OUTPUTS</span></span>

### <span data-ttu-id="eb207-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb207-120">System.Boolean</span></span>

## <span data-ttu-id="eb207-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb207-121">NOTES</span></span>

## <span data-ttu-id="eb207-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb207-122">RELATED LINKS</span></span>

[<span data-ttu-id="eb207-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb207-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="eb207-124">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb207-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


