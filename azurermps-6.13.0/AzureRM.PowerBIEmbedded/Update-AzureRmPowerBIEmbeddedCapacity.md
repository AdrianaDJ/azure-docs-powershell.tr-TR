---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593929"
---
# <span data-ttu-id="4509e-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4509e-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4509e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4509e-102">SYNOPSIS</span></span>
<span data-ttu-id="4509e-103">PowerBI Embedded kapasitesi örneğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4509e-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4509e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4509e-104">SYNTAX</span></span>

### <span data-ttu-id="4509e-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4509e-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4509e-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4509e-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4509e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4509e-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4509e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4509e-108">DESCRIPTION</span></span>
<span data-ttu-id="4509e-109">Update-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="4509e-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4509e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4509e-110">EXAMPLES</span></span>

### <span data-ttu-id="4509e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4509e-111">Example 1</span></span>
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

<span data-ttu-id="4509e-112">Anahtar olarak atamak için resourcegroup testgroup 'daki testcapacity adlı kapasiteyi değiştirir: değer1 ve anahtar2: değer2 ve yönetici testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="4509e-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="4509e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4509e-113">PARAMETERS</span></span>

### <span data-ttu-id="4509e-114">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="4509e-114">-Administrator</span></span>
<span data-ttu-id="4509e-115">Kapasitede yönetici olarak ayarlanacak, virgülle ayrılmış kapasite adları</span><span class="sxs-lookup"><span data-stu-id="4509e-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4509e-116">-DefaultProfile</span></span>
<span data-ttu-id="4509e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4509e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4509e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4509e-118">-InputObject</span></span>
<span data-ttu-id="4509e-119">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="4509e-119">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4509e-120">-Name</span></span>
<span data-ttu-id="4509e-121">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="4509e-121">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4509e-122">-PassThru</span></span>
<span data-ttu-id="4509e-123">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="4509e-123">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4509e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4509e-125">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4509e-125">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4509e-126">-ResourceId</span></span>
<span data-ttu-id="4509e-127">PowerBI Embedded kapasite RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4509e-127">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="4509e-128">-Sku</span></span>
<span data-ttu-id="4509e-129">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="4509e-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4509e-130">-Tag</span></span>
<span data-ttu-id="4509e-131">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4509e-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4509e-132">-Confirm</span></span>
<span data-ttu-id="4509e-133">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="4509e-133">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4509e-134">-WhatIf</span></span>
<span data-ttu-id="4509e-135">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="4509e-135">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4509e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4509e-136">CommonParameters</span></span>
<span data-ttu-id="4509e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4509e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4509e-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4509e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4509e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4509e-139">INPUTS</span></span>

### <span data-ttu-id="4509e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4509e-140">System.String</span></span>

### <span data-ttu-id="4509e-141">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4509e-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="4509e-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4509e-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4509e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4509e-143">OUTPUTS</span></span>

### <span data-ttu-id="4509e-144">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4509e-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4509e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4509e-145">NOTES</span></span>

## <span data-ttu-id="4509e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4509e-146">RELATED LINKS</span></span>

[<span data-ttu-id="4509e-147">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="4509e-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4509e-148">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="4509e-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
