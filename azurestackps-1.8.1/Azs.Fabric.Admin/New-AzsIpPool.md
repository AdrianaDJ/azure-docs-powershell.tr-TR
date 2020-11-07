---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934951"
---
# <span data-ttu-id="26088-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="26088-101">New-AzsIpPool</span></span>

## <span data-ttu-id="26088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26088-102">SYNOPSIS</span></span>
<span data-ttu-id="26088-103">Altyapı IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26088-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="26088-104">Bir IP havuzu oluşturulduktan sonra silinemez veya değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="26088-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="26088-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26088-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26088-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="26088-106">DESCRIPTION</span></span>
<span data-ttu-id="26088-107">Altyapı IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26088-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="26088-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26088-108">EXAMPLES</span></span>

### <span data-ttu-id="26088-109">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="26088-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="26088-110">Yeni bir IP havuzu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26088-110">Create a new IP pool.</span></span>

## <span data-ttu-id="26088-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26088-111">PARAMETERS</span></span>

### <span data-ttu-id="26088-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="26088-112">-Name</span></span>
<span data-ttu-id="26088-113">IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="26088-113">IP pool name.</span></span>

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

### <span data-ttu-id="26088-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="26088-114">-AddressPrefix</span></span>
<span data-ttu-id="26088-115">Adres öneki.</span><span class="sxs-lookup"><span data-stu-id="26088-115">The address prefix.</span></span>

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

### <span data-ttu-id="26088-116">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="26088-116">-StartIpAddress</span></span>
<span data-ttu-id="26088-117">Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="26088-117">The starting IP address.</span></span>

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

### <span data-ttu-id="26088-118">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="26088-118">-EndIpAddress</span></span>
<span data-ttu-id="26088-119">Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="26088-119">The ending IP address.</span></span>

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

### <span data-ttu-id="26088-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="26088-120">-Location</span></span>
<span data-ttu-id="26088-121">Kaynağın bulunduğu bölge.</span><span class="sxs-lookup"><span data-stu-id="26088-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="26088-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26088-122">-ResourceGroupName</span></span>
<span data-ttu-id="26088-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="26088-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="26088-124">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="26088-124">-Tags</span></span>
<span data-ttu-id="26088-125">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="26088-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="26088-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="26088-126">-AsJob</span></span>
<span data-ttu-id="26088-127">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="26088-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="26088-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26088-128">-WhatIf</span></span>
<span data-ttu-id="26088-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26088-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26088-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26088-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26088-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="26088-131">-Confirm</span></span>
<span data-ttu-id="26088-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26088-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26088-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26088-133">CommonParameters</span></span>
<span data-ttu-id="26088-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26088-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26088-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26088-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26088-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26088-136">INPUTS</span></span>

## <span data-ttu-id="26088-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26088-137">OUTPUTS</span></span>

### <span data-ttu-id="26088-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="26088-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="26088-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26088-139">NOTES</span></span>

## <span data-ttu-id="26088-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26088-140">RELATED LINKS</span></span>
