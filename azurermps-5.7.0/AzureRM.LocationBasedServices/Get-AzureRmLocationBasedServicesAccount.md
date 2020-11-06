---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588894"
---
# <span data-ttu-id="b4eca-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4eca-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="b4eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4eca-102">SYNOPSIS</span></span>
<span data-ttu-id="b4eca-103">Hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4eca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4eca-104">SYNTAX</span></span>

### <span data-ttu-id="b4eca-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4eca-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4eca-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4eca-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4eca-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b4eca-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4eca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4eca-108">DESCRIPTION</span></span>
<span data-ttu-id="b4eca-109">**Get-Azurermlocationbasevseçservicesaccount** cmdlet 'i, kaynak grubuna ve adına göre veya kaynak kimliğine göre sağlanan bir konum temelli hizmetler hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="b4eca-110">Ayrıca, geçerli aboneliğin ResourceGroup veya tüm konum tabanlı hizmetler hesaplarında tüm hesapların listesini döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="b4eca-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="b4eca-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4eca-111">EXAMPLES</span></span>

### <span data-ttu-id="b4eca-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4eca-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="b4eca-113">Eğer varsa, MyResourceGroup kaynak grubundaki MyAccount adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="b4eca-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b4eca-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="b4eca-115">MyResourceGroup kaynak grubundaki tüm konum tabanlı hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b4eca-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b4eca-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="b4eca-117">Geçerli abonelikteki tüm konum tabanlı hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="b4eca-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="b4eca-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="b4eca-119">Kaynak kimliği tarafından belirtilen konum tabanlı hizmetler hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="b4eca-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="b4eca-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4eca-120">PARAMETERS</span></span>

### <span data-ttu-id="b4eca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4eca-121">-DefaultProfile</span></span>
<span data-ttu-id="b4eca-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4eca-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4eca-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4eca-123">-Name</span></span>
<span data-ttu-id="b4eca-124">Konum tabanlı hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="b4eca-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4eca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4eca-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4eca-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4eca-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4eca-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4eca-127">-ResourceId</span></span>
<span data-ttu-id="b4eca-128">Konum temelli hizmetler hesabı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="b4eca-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4eca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4eca-129">CommonParameters</span></span>
<span data-ttu-id="b4eca-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4eca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4eca-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4eca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4eca-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4eca-132">INPUTS</span></span>

### <span data-ttu-id="b4eca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b4eca-133">System.String</span></span>

## <span data-ttu-id="b4eca-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4eca-134">OUTPUTS</span></span>

### <span data-ttu-id="b4eca-135">Microsoft. Azure. Commands. Locationbasevseçservices. model. Pslocationbasevseçservicesaccount</span><span class="sxs-lookup"><span data-stu-id="b4eca-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="b4eca-136">Bu cmdlet, **Pslocationbasevseçservicesaccount** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4eca-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="b4eca-137">Bu nesneyi değiştirebilir ve ardından **set-Azurermlocationbasevseçservices** kullanarak değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4eca-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="b4eca-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4eca-138">NOTES</span></span>

## <span data-ttu-id="b4eca-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4eca-139">RELATED LINKS</span></span>
