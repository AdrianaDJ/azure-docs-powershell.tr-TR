---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573390"
---
# <span data-ttu-id="6fda5-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6fda5-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6fda5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fda5-102">SYNOPSIS</span></span>
<span data-ttu-id="6fda5-103">PowerBI Embedded kapasitesi örneğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6fda5-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fda5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fda5-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="6fda5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fda5-105">DESCRIPTION</span></span>
<span data-ttu-id="6fda5-106">Update-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="6fda5-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="6fda5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fda5-107">EXAMPLES</span></span>

### <span data-ttu-id="6fda5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fda5-108">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}

```

<span data-ttu-id="6fda5-109">Anahtar olarak atamak için resourcegroup testgroup 'daki testcapacity adlı kapasiteyi değiştirir: değer1 ve anahtar2: değer2 ve yönetici testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6fda5-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="6fda5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fda5-110">PARAMETERS</span></span>

### <span data-ttu-id="6fda5-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fda5-111">-Name</span></span>
<span data-ttu-id="6fda5-112">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="6fda5-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fda5-113">-ResourceGroupName</span></span>
<span data-ttu-id="6fda5-114">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6fda5-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="6fda5-115">-Sku</span></span>
<span data-ttu-id="6fda5-116">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="6fda5-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-117">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6fda5-117">-Tag</span></span>
<span data-ttu-id="6fda5-118">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6fda5-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="6fda5-119">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="6fda5-119">-Administrator</span></span>
<span data-ttu-id="6fda5-120">Kapasitede yönetici olarak ayarlanacak, virgülle ayrılmış kapasite adları</span><span class="sxs-lookup"><span data-stu-id="6fda5-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fda5-121">-ResourceId</span></span>
<span data-ttu-id="6fda5-122">PowerBI Embedded kapasite RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="6fda5-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fda5-123">-InputObject</span></span>
<span data-ttu-id="6fda5-124">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fda5-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6fda5-125">-PassThru</span></span>
<span data-ttu-id="6fda5-126">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="6fda5-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fda5-127">-Confirm</span></span>
<span data-ttu-id="6fda5-128">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="6fda5-128">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fda5-129">-WhatIf</span></span>
<span data-ttu-id="6fda5-130">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="6fda5-130">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fda5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fda5-131">CommonParameters</span></span>
<span data-ttu-id="6fda5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fda5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fda5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fda5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fda5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fda5-134">INPUTS</span></span>

### <span data-ttu-id="6fda5-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6fda5-135">None</span></span>
<span data-ttu-id="6fda5-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6fda5-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6fda5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fda5-137">OUTPUTS</span></span>

### <span data-ttu-id="6fda5-138">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6fda5-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6fda5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fda5-139">NOTES</span></span>

## <span data-ttu-id="6fda5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fda5-140">RELATED LINKS</span></span>

[<span data-ttu-id="6fda5-141">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="6fda5-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6fda5-142">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="6fda5-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
