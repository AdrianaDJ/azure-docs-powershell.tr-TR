---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593991"
---
# <span data-ttu-id="870fa-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="870fa-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="870fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870fa-102">SYNOPSIS</span></span>
<span data-ttu-id="870fa-103">Hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="870fa-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="870fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="870fa-104">SYNTAX</span></span>

### <span data-ttu-id="870fa-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="870fa-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="870fa-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="870fa-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="870fa-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="870fa-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="870fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="870fa-108">DESCRIPTION</span></span>
<span data-ttu-id="870fa-109">Get-AzureRmMapsAccount cmdlet 'i, kaynak grubu ile ad veya kaynak kimliği tarafından sağlanan Azure haritaları hesabını alır. Ayrıca, geçerli aboneliğin ResourceGroup veya tüm Azure haritalar hesaplarında tüm hesapların bir listesini döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="870fa-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="870fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="870fa-110">EXAMPLES</span></span>

### <span data-ttu-id="870fa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="870fa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="870fa-112">Eğer varsa, MyResourceGroup kaynak grubundaki MyAccount adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="870fa-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="870fa-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="870fa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="870fa-114">MyResourceGroup kaynak grubundaki tüm Azure haritalar hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="870fa-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="870fa-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="870fa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="870fa-116">Geçerli abonelikteki tüm Azure haritalar hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="870fa-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="870fa-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="870fa-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="870fa-118">Kaynak kimliği tarafından belirtilen haritalar hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="870fa-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="870fa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="870fa-119">PARAMETERS</span></span>

### <span data-ttu-id="870fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870fa-120">-DefaultProfile</span></span>
<span data-ttu-id="870fa-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="870fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="870fa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="870fa-122">-Name</span></span>
<span data-ttu-id="870fa-123">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="870fa-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="870fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="870fa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="870fa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="870fa-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="870fa-126">-ResourceId</span></span>
<span data-ttu-id="870fa-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="870fa-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="870fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870fa-128">CommonParameters</span></span>
<span data-ttu-id="870fa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="870fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870fa-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870fa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="870fa-131">INPUTS</span></span>

### <span data-ttu-id="870fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="870fa-132">System.String</span></span>

## <span data-ttu-id="870fa-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="870fa-133">OUTPUTS</span></span>

### <span data-ttu-id="870fa-134">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="870fa-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="870fa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="870fa-135">NOTES</span></span>

## <span data-ttu-id="870fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="870fa-136">RELATED LINKS</span></span>
