---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934110"
---
# <span data-ttu-id="a98de-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="a98de-101">New-AzsIpPool</span></span>

## <span data-ttu-id="a98de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98de-102">SYNOPSIS</span></span>
<span data-ttu-id="a98de-103">Altyapı IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a98de-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="a98de-104">Bir IP havuzu oluşturulduktan sonra silinemez veya değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="a98de-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="a98de-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a98de-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a98de-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="a98de-106">DESCRIPTION</span></span>
<span data-ttu-id="a98de-107">Altyapı IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a98de-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="a98de-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a98de-108">EXAMPLES</span></span>

### <span data-ttu-id="a98de-109">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a98de-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="a98de-110">Yeni bir IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a98de-110">Create a new IP pool.</span></span>

## <span data-ttu-id="a98de-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a98de-111">PARAMETERS</span></span>

### <span data-ttu-id="a98de-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a98de-112">-AddressPrefix</span></span>
<span data-ttu-id="a98de-113">Adres öneki.</span><span class="sxs-lookup"><span data-stu-id="a98de-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a98de-114">-AsJob</span></span>
<span data-ttu-id="a98de-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="a98de-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-116">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="a98de-116">-EndIpAddress</span></span>
<span data-ttu-id="a98de-117">Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="a98de-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a98de-118">-Location</span></span>
<span data-ttu-id="a98de-119">Kaynağın bulunduğu bölge.</span><span class="sxs-lookup"><span data-stu-id="a98de-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a98de-120">-Name</span></span>
<span data-ttu-id="a98de-121">IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="a98de-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98de-122">-ResourceGroupName</span></span>
<span data-ttu-id="a98de-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a98de-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-124">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="a98de-124">-StartIpAddress</span></span>
<span data-ttu-id="a98de-125">Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="a98de-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="a98de-126">-Tags</span></span>
<span data-ttu-id="a98de-127">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="a98de-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98de-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a98de-128">-Confirm</span></span>
<span data-ttu-id="a98de-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a98de-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a98de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a98de-130">-WhatIf</span></span>
<span data-ttu-id="a98de-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a98de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a98de-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a98de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a98de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98de-133">CommonParameters</span></span>
<span data-ttu-id="a98de-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a98de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98de-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a98de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98de-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a98de-136">INPUTS</span></span>

## <span data-ttu-id="a98de-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a98de-137">OUTPUTS</span></span>

### <span data-ttu-id="a98de-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="a98de-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="a98de-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a98de-139">NOTES</span></span>

## <span data-ttu-id="a98de-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a98de-140">RELATED LINKS</span></span>

