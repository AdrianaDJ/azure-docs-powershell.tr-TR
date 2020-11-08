---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108941"
---
# <span data-ttu-id="b7078-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b7078-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="b7078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7078-102">SYNOPSIS</span></span>
<span data-ttu-id="b7078-103">Custobir önek kaynağı alır</span><span class="sxs-lookup"><span data-stu-id="b7078-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="b7078-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7078-104">SYNTAX</span></span>

### <span data-ttu-id="b7078-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7078-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7078-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b7078-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7078-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7078-107">DESCRIPTION</span></span>
<span data-ttu-id="b7078-108">**Get-Azcustomhttp önek** cmdlet 'i, giriş parametreleri kümesi</span><span class="sxs-lookup"><span data-stu-id="b7078-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="b7078-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7078-109">EXAMPLES</span></span>

### <span data-ttu-id="b7078-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7078-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="b7078-111">Bu komut, kaynak grubunda MyCustom</span><span class="sxs-lookup"><span data-stu-id="b7078-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="b7078-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7078-112">PARAMETERS</span></span>

### <span data-ttu-id="b7078-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7078-113">-DefaultProfile</span></span>
<span data-ttu-id="b7078-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7078-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7078-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7078-115">-Name</span></span>
<span data-ttu-id="b7078-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b7078-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7078-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7078-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7078-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b7078-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7078-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7078-119">-ResourceId</span></span>
<span data-ttu-id="b7078-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b7078-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7078-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7078-121">CommonParameters</span></span>
<span data-ttu-id="b7078-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7078-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7078-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7078-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7078-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7078-124">INPUTS</span></span>

### <span data-ttu-id="b7078-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b7078-125">System.String</span></span>

## <span data-ttu-id="b7078-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7078-126">OUTPUTS</span></span>

### <span data-ttu-id="b7078-127">Microsoft. Azure. Commands. Network. model. Pscustolermi öneki</span><span class="sxs-lookup"><span data-stu-id="b7078-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="b7078-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7078-128">NOTES</span></span>

## <span data-ttu-id="b7078-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7078-129">RELATED LINKS</span></span>

[<span data-ttu-id="b7078-130">Yeni-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="b7078-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="b7078-131">Remove-Azcustomhttp öneki</span><span class="sxs-lookup"><span data-stu-id="b7078-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="b7078-132">Update-Azcustombu önek</span><span class="sxs-lookup"><span data-stu-id="b7078-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)