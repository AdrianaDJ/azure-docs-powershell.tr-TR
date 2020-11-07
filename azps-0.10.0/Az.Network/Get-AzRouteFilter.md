---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935487"
---
# <span data-ttu-id="d087e-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d087e-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="d087e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d087e-102">SYNOPSIS</span></span>
<span data-ttu-id="d087e-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="d087e-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="d087e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d087e-104">SYNTAX</span></span>

### <span data-ttu-id="d087e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="d087e-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d087e-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="d087e-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d087e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d087e-107">DESCRIPTION</span></span>
<span data-ttu-id="d087e-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="d087e-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d087e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d087e-109">EXAMPLES</span></span>

### <span data-ttu-id="d087e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d087e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d087e-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="d087e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d087e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d087e-112">PARAMETERS</span></span>

### <span data-ttu-id="d087e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d087e-113">-DefaultProfile</span></span>
<span data-ttu-id="d087e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d087e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d087e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d087e-115">-ExpandResource</span></span>
<span data-ttu-id="d087e-116">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="d087e-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="d087e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d087e-117">-Name</span></span>
<span data-ttu-id="d087e-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d087e-118">The resource name.</span></span>

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

### <span data-ttu-id="d087e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d087e-119">-ResourceGroupName</span></span>
<span data-ttu-id="d087e-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d087e-120">The resource group name.</span></span>

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

### <span data-ttu-id="d087e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d087e-121">CommonParameters</span></span>
<span data-ttu-id="d087e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d087e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d087e-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d087e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d087e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d087e-124">INPUTS</span></span>

### <span data-ttu-id="d087e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d087e-125">System.String</span></span>

## <span data-ttu-id="d087e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d087e-126">OUTPUTS</span></span>

### <span data-ttu-id="d087e-127">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d087e-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d087e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d087e-128">NOTES</span></span>

## <span data-ttu-id="d087e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d087e-129">RELATED LINKS</span></span>

