---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3f2515a1c1039dbf9ff4a0635111c95a610d9834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932806"
---
# <span data-ttu-id="64bc7-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64bc7-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="64bc7-103">Yeni bir PowerBI Embedded kapasitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64bc7-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="64bc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64bc7-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bc7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="64bc7-106">New-AzPowerBIEmbeddedCapacity cmdlet 'i yeni bir PowerBI Embedded kapasitesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="64bc7-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="64bc7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="64bc7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="64bc7-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="64bc7-109">ABD merkezi merkezi 'nde ve kaynak grubu testRG 'de testcapacity adlı bir kapasite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64bc7-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="64bc7-110">Kapasite için SKU düzeyi a1 olur.</span><span class="sxs-lookup"><span data-stu-id="64bc7-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="64bc7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64bc7-111">PARAMETERS</span></span>

### <span data-ttu-id="64bc7-112">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="64bc7-112">-Administrator</span></span>
<span data-ttu-id="64bc7-113">Kapasitede yönetici olarak ayarlanacak virgülle ayrılmış adlar</span><span class="sxs-lookup"><span data-stu-id="64bc7-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bc7-114">-DefaultProfile</span></span>
<span data-ttu-id="64bc7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64bc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64bc7-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="64bc7-116">-Location</span></span>
<span data-ttu-id="64bc7-117">PowerBI Embedded kapasitesinin barındırıldığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="64bc7-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="64bc7-118">-Name</span></span>
<span data-ttu-id="64bc7-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="64bc7-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bc7-120">-ResourceGroupName</span></span>
<span data-ttu-id="64bc7-121">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="64bc7-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="64bc7-122">-Sku</span></span>
<span data-ttu-id="64bc7-123">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="64bc7-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="64bc7-124">-Tag</span></span>
<span data-ttu-id="64bc7-125">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="64bc7-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc7-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="64bc7-126">-Confirm</span></span>
<span data-ttu-id="64bc7-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="64bc7-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="64bc7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bc7-128">-WhatIf</span></span>
<span data-ttu-id="64bc7-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="64bc7-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="64bc7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bc7-130">CommonParameters</span></span>
<span data-ttu-id="64bc7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64bc7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bc7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bc7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bc7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64bc7-133">INPUTS</span></span>

### <span data-ttu-id="64bc7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="64bc7-134">System.String</span></span>

### <span data-ttu-id="64bc7-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="64bc7-135">System.String[]</span></span>

### <span data-ttu-id="64bc7-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64bc7-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64bc7-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64bc7-137">OUTPUTS</span></span>

### <span data-ttu-id="64bc7-138">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64bc7-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64bc7-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64bc7-139">NOTES</span></span>

## <span data-ttu-id="64bc7-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64bc7-140">RELATED LINKS</span></span>

[<span data-ttu-id="64bc7-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64bc7-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="64bc7-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64bc7-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
