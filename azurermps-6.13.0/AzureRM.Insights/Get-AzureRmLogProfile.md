---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594410"
---
# <span data-ttu-id="f641f-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f641f-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="f641f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f641f-102">SYNOPSIS</span></span>
<span data-ttu-id="f641f-103">Günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="f641f-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f641f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f641f-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f641f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f641f-105">DESCRIPTION</span></span>
<span data-ttu-id="f641f-106">**Get-AzureRmLogProfile** cmdlet 'i bir günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="f641f-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="f641f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f641f-107">EXAMPLES</span></span>

## <span data-ttu-id="f641f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f641f-108">PARAMETERS</span></span>

### <span data-ttu-id="f641f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f641f-109">-DefaultProfile</span></span>
<span data-ttu-id="f641f-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f641f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f641f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="f641f-111">-Name</span></span>
<span data-ttu-id="f641f-112">Alınacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f641f-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f641f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f641f-113">CommonParameters</span></span>
<span data-ttu-id="f641f-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f641f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f641f-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f641f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f641f-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f641f-116">INPUTS</span></span>

### <span data-ttu-id="f641f-117">System. String</span><span class="sxs-lookup"><span data-stu-id="f641f-117">System.String</span></span>

## <span data-ttu-id="f641f-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f641f-118">OUTPUTS</span></span>

### <span data-ttu-id="f641f-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="f641f-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="f641f-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f641f-120">NOTES</span></span>

## <span data-ttu-id="f641f-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f641f-121">RELATED LINKS</span></span>

[<span data-ttu-id="f641f-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f641f-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="f641f-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f641f-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


