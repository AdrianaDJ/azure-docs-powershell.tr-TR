---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109944"
---
# <span data-ttu-id="0af08-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="0af08-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="0af08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af08-102">SYNOPSIS</span></span>
<span data-ttu-id="0af08-103">Uzamsal bağlayıcı hesabının anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="0af08-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="0af08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0af08-104">SYNTAX</span></span>

### <span data-ttu-id="0af08-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0af08-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af08-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0af08-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af08-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="0af08-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af08-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0af08-108">DESCRIPTION</span></span>
<span data-ttu-id="0af08-109">Uzamsal bağlayıcı hesabının geliştirici anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="0af08-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="0af08-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0af08-110">EXAMPLES</span></span>

### <span data-ttu-id="0af08-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0af08-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="0af08-112">Geçerli aboneliğin ve "RG1" kaynak grubundan "örnek" uzamsal bağlayıcı hesaplarının geliştirici anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="0af08-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="0af08-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0af08-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="0af08-114">Geçerli aboneliğin ve "RG1" kaynak grubundan yöneltme ile "örnek" Geliştirici anahtarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="0af08-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="0af08-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0af08-115">PARAMETERS</span></span>

### <span data-ttu-id="0af08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af08-116">-DefaultProfile</span></span>
<span data-ttu-id="0af08-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0af08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0af08-118">-InputObject</span></span>
<span data-ttu-id="0af08-119">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0af08-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0af08-120">-Name</span></span>
<span data-ttu-id="0af08-121">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="0af08-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af08-122">-ResourceGroupName</span></span>
<span data-ttu-id="0af08-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0af08-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0af08-124">-ResourceId</span></span>
<span data-ttu-id="0af08-125">Uzamsal bağlayıcı hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0af08-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af08-126">CommonParameters</span></span>
<span data-ttu-id="0af08-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0af08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0af08-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af08-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af08-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0af08-129">INPUTS</span></span>

### <span data-ttu-id="0af08-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0af08-130">System.String</span></span>

### <span data-ttu-id="0af08-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="0af08-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="0af08-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0af08-132">OUTPUTS</span></span>

### <span data-ttu-id="0af08-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0af08-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="0af08-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0af08-134">NOTES</span></span>

## <span data-ttu-id="0af08-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0af08-135">RELATED LINKS</span></span>
