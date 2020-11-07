---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915731"
---
# <span data-ttu-id="c535c-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c535c-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="c535c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c535c-102">SYNOPSIS</span></span>
<span data-ttu-id="c535c-103">Uzamsal bağlayıcı hesabının anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c535c-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="c535c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c535c-104">SYNTAX</span></span>

### <span data-ttu-id="c535c-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c535c-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c535c-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c535c-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c535c-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="c535c-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c535c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c535c-108">DESCRIPTION</span></span>
<span data-ttu-id="c535c-109">Uzamsal bağlayıcı hesabının geliştirici anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="c535c-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="c535c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c535c-110">EXAMPLES</span></span>

### <span data-ttu-id="c535c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c535c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c535c-112">Geçerli aboneliğin ve "RG1" kaynak grubundan "örnek" uzamsal bağlayıcı hesaplarının geliştirici anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="c535c-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="c535c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c535c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c535c-114">Geçerli aboneliğin ve "RG1" kaynak grubundan yöneltme ile "örnek" Geliştirici anahtarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="c535c-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="c535c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c535c-115">PARAMETERS</span></span>

### <span data-ttu-id="c535c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c535c-116">-DefaultProfile</span></span>
<span data-ttu-id="c535c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c535c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c535c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c535c-118">-InputObject</span></span>
<span data-ttu-id="c535c-119">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c535c-119">The custom domain object.</span></span>

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

### <span data-ttu-id="c535c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c535c-120">-Name</span></span>
<span data-ttu-id="c535c-121">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c535c-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="c535c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c535c-122">-ResourceGroupName</span></span>
<span data-ttu-id="c535c-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c535c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c535c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c535c-124">-ResourceId</span></span>
<span data-ttu-id="c535c-125">Uzamsal bağlayıcı hesabının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c535c-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="c535c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c535c-126">CommonParameters</span></span>
<span data-ttu-id="c535c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c535c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c535c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c535c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c535c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c535c-129">INPUTS</span></span>

### <span data-ttu-id="c535c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c535c-130">System.String</span></span>

### <span data-ttu-id="c535c-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c535c-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c535c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c535c-132">OUTPUTS</span></span>

### <span data-ttu-id="c535c-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c535c-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="c535c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c535c-134">NOTES</span></span>

## <span data-ttu-id="c535c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c535c-135">RELATED LINKS</span></span>
