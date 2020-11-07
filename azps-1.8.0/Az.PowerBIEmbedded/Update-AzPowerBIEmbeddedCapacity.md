---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759788"
---
# <span data-ttu-id="34185-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="34185-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="34185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34185-102">SYNOPSIS</span></span>
<span data-ttu-id="34185-103">PowerBI Embedded kapasitesi örneğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="34185-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="34185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34185-104">SYNTAX</span></span>

### <span data-ttu-id="34185-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34185-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34185-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="34185-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34185-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="34185-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34185-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34185-108">DESCRIPTION</span></span>
<span data-ttu-id="34185-109">Update-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="34185-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="34185-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34185-110">EXAMPLES</span></span>

### <span data-ttu-id="34185-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34185-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="34185-112">Anahtar olarak atamak için resourcegroup testgroup 'daki testcapacity adlı kapasiteyi değiştirir: değer1 ve anahtar2: değer2 ve yönetici testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="34185-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="34185-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34185-113">PARAMETERS</span></span>

### <span data-ttu-id="34185-114">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="34185-114">-Administrator</span></span>
<span data-ttu-id="34185-115">Kapasitede yönetici olarak ayarlanacak, virgülle ayrılmış kapasite adları</span><span class="sxs-lookup"><span data-stu-id="34185-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="34185-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34185-116">-DefaultProfile</span></span>
<span data-ttu-id="34185-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34185-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34185-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34185-118">-InputObject</span></span>
<span data-ttu-id="34185-119">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="34185-119">Input object for Piping</span></span>

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

### <span data-ttu-id="34185-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="34185-120">-Name</span></span>
<span data-ttu-id="34185-121">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="34185-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="34185-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34185-122">-PassThru</span></span>
<span data-ttu-id="34185-123">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="34185-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="34185-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34185-124">-ResourceGroupName</span></span>
<span data-ttu-id="34185-125">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="34185-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="34185-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34185-126">-ResourceId</span></span>
<span data-ttu-id="34185-127">PowerBI Embedded kapasite RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="34185-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="34185-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="34185-128">-Sku</span></span>
<span data-ttu-id="34185-129">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="34185-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="34185-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="34185-130">-Tag</span></span>
<span data-ttu-id="34185-131">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="34185-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="34185-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="34185-132">-Confirm</span></span>
<span data-ttu-id="34185-133">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="34185-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="34185-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34185-134">-WhatIf</span></span>
<span data-ttu-id="34185-135">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="34185-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="34185-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34185-136">CommonParameters</span></span>
<span data-ttu-id="34185-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34185-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34185-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34185-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34185-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34185-139">INPUTS</span></span>

### <span data-ttu-id="34185-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34185-140">System.String</span></span>

### <span data-ttu-id="34185-141">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="34185-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="34185-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34185-142">OUTPUTS</span></span>

### <span data-ttu-id="34185-143">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="34185-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="34185-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34185-144">NOTES</span></span>

## <span data-ttu-id="34185-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34185-145">RELATED LINKS</span></span>

[<span data-ttu-id="34185-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="34185-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="34185-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="34185-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
