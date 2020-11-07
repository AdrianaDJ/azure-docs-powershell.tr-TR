---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940066"
---
# <span data-ttu-id="dda9a-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dda9a-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="dda9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dda9a-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="dda9a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dda9a-104">SYNTAX</span></span>

### <span data-ttu-id="dda9a-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="dda9a-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dda9a-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="dda9a-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dda9a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dda9a-107">DESCRIPTION</span></span>
<span data-ttu-id="dda9a-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="dda9a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="dda9a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dda9a-109">EXAMPLES</span></span>

### <span data-ttu-id="dda9a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dda9a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dda9a-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="dda9a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="dda9a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dda9a-112">PARAMETERS</span></span>

### <span data-ttu-id="dda9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda9a-113">-DefaultProfile</span></span>
<span data-ttu-id="dda9a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dda9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda9a-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dda9a-115">-ExpandResource</span></span>
<span data-ttu-id="dda9a-116">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="dda9a-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda9a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="dda9a-117">-Name</span></span>
<span data-ttu-id="dda9a-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="dda9a-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="dda9a-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dda9a-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda9a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda9a-121">CommonParameters</span></span>
<span data-ttu-id="dda9a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dda9a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda9a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda9a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda9a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dda9a-124">INPUTS</span></span>

### <span data-ttu-id="dda9a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dda9a-125">System.String</span></span>

## <span data-ttu-id="dda9a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dda9a-126">OUTPUTS</span></span>

### <span data-ttu-id="dda9a-127">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dda9a-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="dda9a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dda9a-128">NOTES</span></span>

## <span data-ttu-id="dda9a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dda9a-129">RELATED LINKS</span></span>

