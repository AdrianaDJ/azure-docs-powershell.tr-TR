---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279658"
---
# <span data-ttu-id="54c09-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="54c09-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="54c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c09-102">SYNOPSIS</span></span>
<span data-ttu-id="54c09-103">Azure IP ayırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54c09-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="54c09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54c09-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54c09-105">DESCRIPTION</span></span>
<span data-ttu-id="54c09-106">**Yeni-Azıpallocation** cmdlet 'ı bir Azure IP ayırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="54c09-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="54c09-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54c09-107">EXAMPLES</span></span>

### <span data-ttu-id="54c09-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54c09-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="54c09-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54c09-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="54c09-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54c09-110">PARAMETERS</span></span>

### <span data-ttu-id="54c09-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="54c09-111">-AsJob</span></span>
<span data-ttu-id="54c09-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="54c09-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54c09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c09-113">-DefaultProfile</span></span>
<span data-ttu-id="54c09-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54c09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c09-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54c09-115">-Force</span></span>
<span data-ttu-id="54c09-116">Kaynağı geçersiz kılmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="54c09-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="54c09-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="54c09-117">-IpAllocationTag</span></span>
<span data-ttu-id="54c09-118">IP ayırmanın ayırma etiketleri</span><span class="sxs-lookup"><span data-stu-id="54c09-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="54c09-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="54c09-119">-IpAllocationType</span></span>
<span data-ttu-id="54c09-120">IP ayırma türü</span><span class="sxs-lookup"><span data-stu-id="54c09-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-121">-Ipamalkonumkimliği</span><span class="sxs-lookup"><span data-stu-id="54c09-121">-IpamAllocationId</span></span>
<span data-ttu-id="54c09-122">IP ayırmanın IPAM ayırma KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="54c09-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="54c09-123">-Location</span></span>
<span data-ttu-id="54c09-124">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="54c09-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="54c09-125">-Name</span></span>
<span data-ttu-id="54c09-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="54c09-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-127">-Önek</span><span class="sxs-lookup"><span data-stu-id="54c09-127">-Prefix</span></span>
<span data-ttu-id="54c09-128">IP ayırmanın öneki</span><span class="sxs-lookup"><span data-stu-id="54c09-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="54c09-129">-PrefixLength</span></span>
<span data-ttu-id="54c09-130">IP ayırmanın önek uzunluğu</span><span class="sxs-lookup"><span data-stu-id="54c09-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="54c09-131">-PrefixType</span></span>
<span data-ttu-id="54c09-132">IP ayırmanın önek türü</span><span class="sxs-lookup"><span data-stu-id="54c09-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c09-133">-ResourceGroupName</span></span>
<span data-ttu-id="54c09-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="54c09-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c09-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="54c09-135">-Tag</span></span>
<span data-ttu-id="54c09-136">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="54c09-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="54c09-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="54c09-137">-Confirm</span></span>
<span data-ttu-id="54c09-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54c09-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c09-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c09-139">-WhatIf</span></span>
<span data-ttu-id="54c09-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54c09-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c09-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54c09-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c09-142">CommonParameters</span></span>
<span data-ttu-id="54c09-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54c09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c09-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54c09-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c09-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54c09-145">INPUTS</span></span>

### <span data-ttu-id="54c09-146">System. String</span><span class="sxs-lookup"><span data-stu-id="54c09-146">System.String</span></span>

### <span data-ttu-id="54c09-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54c09-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="54c09-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54c09-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="54c09-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54c09-149">OUTPUTS</span></span>

### <span data-ttu-id="54c09-150">Microsoft. Azure. Commands. Network. model. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="54c09-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="54c09-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54c09-151">NOTES</span></span>

## <span data-ttu-id="54c09-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54c09-152">RELATED LINKS</span></span>
