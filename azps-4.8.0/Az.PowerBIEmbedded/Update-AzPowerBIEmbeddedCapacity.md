---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109394"
---
# <span data-ttu-id="e3ad4-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e3ad4-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e3ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ad4-103">PowerBI Embedded kapasitesi örneğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e3ad4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3ad4-104">SYNTAX</span></span>

### <span data-ttu-id="e3ad4-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3ad4-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ad4-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e3ad4-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3ad4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e3ad4-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ad4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="e3ad4-109">Update-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini değiştirir</span><span class="sxs-lookup"><span data-stu-id="e3ad4-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e3ad4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="e3ad4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3ad4-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="e3ad4-112">Anahtar olarak atamak için resourcegroup testgroup 'daki testcapacity adındaki kapasiteyi değiştirir: değer1 ve anahtar2: değer2 ve yöneticiyi kime testuser1@contoso.com testuser2@contoso.com ve hizmet sorumlusu: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="e3ad4-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="e3ad4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3ad4-113">PARAMETERS</span></span>

### <span data-ttu-id="e3ad4-114">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="e3ad4-114">-Administrator</span></span>
<span data-ttu-id="e3ad4-115">Kapasitede yönetici olarak ayarlanacak virgülle ayrılmış adlar.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="e3ad4-116">Hizmet sorumlusu için: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="e3ad4-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="e3ad4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ad4-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ad4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ad4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3ad4-119">-InputObject</span></span>
<span data-ttu-id="e3ad4-120">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="e3ad4-120">Input object for Piping</span></span>

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

### <span data-ttu-id="e3ad4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3ad4-121">-Name</span></span>
<span data-ttu-id="e3ad4-122">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="e3ad4-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e3ad4-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3ad4-123">-PassThru</span></span>
<span data-ttu-id="e3ad4-124">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="e3ad4-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e3ad4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ad4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3ad4-126">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e3ad4-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e3ad4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e3ad4-127">-ResourceId</span></span>
<span data-ttu-id="e3ad4-128">PowerBI Embedded kapasite RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="e3ad4-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3ad4-129">-Sku</span></span>
<span data-ttu-id="e3ad4-130">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="e3ad4-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e3ad4-131">-Tag</span></span>
<span data-ttu-id="e3ad4-132">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="e3ad4-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3ad4-133">-Confirm</span></span>
<span data-ttu-id="e3ad4-134">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="e3ad4-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e3ad4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ad4-135">-WhatIf</span></span>
<span data-ttu-id="e3ad4-136">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="e3ad4-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e3ad4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ad4-137">CommonParameters</span></span>
<span data-ttu-id="e3ad4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3ad4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ad4-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ad4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ad4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3ad4-140">INPUTS</span></span>

### <span data-ttu-id="e3ad4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3ad4-141">System.String</span></span>

### <span data-ttu-id="e3ad4-142">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e3ad4-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e3ad4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3ad4-143">OUTPUTS</span></span>

### <span data-ttu-id="e3ad4-144">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e3ad4-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e3ad4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3ad4-145">NOTES</span></span>

## <span data-ttu-id="e3ad4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3ad4-146">RELATED LINKS</span></span>

[<span data-ttu-id="e3ad4-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e3ad4-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e3ad4-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e3ad4-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
