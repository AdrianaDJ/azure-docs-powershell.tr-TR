---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 35f63b4655b92e42eb0a7d1bae70e2ef01c57a02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590165"
---
# <span data-ttu-id="1dde2-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dde2-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1dde2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dde2-102">SYNOPSIS</span></span>
<span data-ttu-id="1dde2-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1dde2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dde2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dde2-104">SYNTAX</span></span>

### <span data-ttu-id="1dde2-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="1dde2-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dde2-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="1dde2-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dde2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dde2-107">DESCRIPTION</span></span>
<span data-ttu-id="1dde2-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1dde2-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1dde2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dde2-109">EXAMPLES</span></span>

### <span data-ttu-id="1dde2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dde2-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1dde2-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="1dde2-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1dde2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dde2-112">PARAMETERS</span></span>

### <span data-ttu-id="1dde2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dde2-113">-DefaultProfile</span></span>
<span data-ttu-id="1dde2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dde2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dde2-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1dde2-115">-ExpandResource</span></span>
<span data-ttu-id="1dde2-116">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="1dde2-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dde2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dde2-117">-Name</span></span>
<span data-ttu-id="1dde2-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1dde2-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dde2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dde2-119">-ResourceGroupName</span></span>
<span data-ttu-id="1dde2-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1dde2-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dde2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dde2-121">CommonParameters</span></span>
<span data-ttu-id="1dde2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dde2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dde2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dde2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dde2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dde2-124">INPUTS</span></span>

### <span data-ttu-id="1dde2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1dde2-125">System.String</span></span>

## <span data-ttu-id="1dde2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dde2-126">OUTPUTS</span></span>

### <span data-ttu-id="1dde2-127">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dde2-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1dde2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dde2-128">NOTES</span></span>

## <span data-ttu-id="1dde2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dde2-129">RELATED LINKS</span></span>
