---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 7ea94e2e7e4c3e54d67beef367dffee001e94652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915800"
---
# <span data-ttu-id="05dc3-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="05dc3-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="05dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="05dc3-103">Hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="05dc3-103">Gets the account.</span></span>

## <span data-ttu-id="05dc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05dc3-104">SYNTAX</span></span>

### <span data-ttu-id="05dc3-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05dc3-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05dc3-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05dc3-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05dc3-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="05dc3-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05dc3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="05dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="05dc3-109">Get-AzMapsAccount cmdlet 'i, kaynak grubu ile ad veya kaynak kimliği tarafından sağlanan Azure haritaları hesabını alır. Ayrıca, geçerli aboneliğin ResourceGroup veya tüm Azure haritalar hesaplarında tüm hesapların bir listesini döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="05dc3-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="05dc3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05dc3-110">EXAMPLES</span></span>

### <span data-ttu-id="05dc3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05dc3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="05dc3-112">Eğer varsa, MyResourceGroup kaynak grubundaki MyAccount adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="05dc3-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="05dc3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="05dc3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="05dc3-114">MyResourceGroup kaynak grubundaki tüm Azure haritalar hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="05dc3-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="05dc3-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="05dc3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="05dc3-116">Geçerli abonelikteki tüm Azure haritalar hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="05dc3-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="05dc3-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="05dc3-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="05dc3-118">Kaynak kimliği tarafından belirtilen haritalar hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="05dc3-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="05dc3-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05dc3-119">PARAMETERS</span></span>

### <span data-ttu-id="05dc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05dc3-120">-DefaultProfile</span></span>
<span data-ttu-id="05dc3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05dc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dc3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="05dc3-122">-Name</span></span>
<span data-ttu-id="05dc3-123">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="05dc3-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05dc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05dc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="05dc3-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="05dc3-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05dc3-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="05dc3-126">-ResourceId</span></span>
<span data-ttu-id="05dc3-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="05dc3-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05dc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dc3-128">CommonParameters</span></span>
<span data-ttu-id="05dc3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05dc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dc3-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05dc3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dc3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05dc3-131">INPUTS</span></span>

### <span data-ttu-id="05dc3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05dc3-132">System.String</span></span>

## <span data-ttu-id="05dc3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05dc3-133">OUTPUTS</span></span>

### <span data-ttu-id="05dc3-134">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="05dc3-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="05dc3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05dc3-135">NOTES</span></span>

## <span data-ttu-id="05dc3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05dc3-136">RELATED LINKS</span></span>
