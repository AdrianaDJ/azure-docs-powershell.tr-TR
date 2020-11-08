---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098548"
---
# <span data-ttu-id="d97e2-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d97e2-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="d97e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d97e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d97e2-103">Bir cihaz için yeni bir sıra oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d97e2-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="d97e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d97e2-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d97e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d97e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d97e2-106">**Yeni-AzStackEdgeOrder** cmdlet 'ı yığın uç aygıtı için yeni bir sıra oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d97e2-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="d97e2-107">Bir sıra oluşturmadan önce bir yığın uç cihaz kaynağının oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d97e2-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="d97e2-108">İlgili kişi, şirket adı, e-posta, adres vb. gibi ayrıntıları, siparişi oluşturmaya yönelik parametreler olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d97e2-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="d97e2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d97e2-109">EXAMPLES</span></span>

### <span data-ttu-id="d97e2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d97e2-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d97e2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d97e2-111">PARAMETERS</span></span>

### <span data-ttu-id="d97e2-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="d97e2-112">-AddressLine1</span></span>
<span data-ttu-id="d97e2-113">Adres ilk satırı</span><span class="sxs-lookup"><span data-stu-id="d97e2-113">Address first line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="d97e2-114">-AddressLine2</span></span>
<span data-ttu-id="d97e2-115">Adres ikinci satırı</span><span class="sxs-lookup"><span data-stu-id="d97e2-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="d97e2-116">-AddressLine3</span></span>
<span data-ttu-id="d97e2-117">Adres üçüncü satır</span><span class="sxs-lookup"><span data-stu-id="d97e2-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="d97e2-118">-AsJob</span></span>
<span data-ttu-id="d97e2-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d97e2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d97e2-120">-Şehir</span><span class="sxs-lookup"><span data-stu-id="d97e2-120">-City</span></span>
<span data-ttu-id="d97e2-121">Şehrin adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-121">Name of the City</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-122">-ŞirketAdı</span><span class="sxs-lookup"><span data-stu-id="d97e2-122">-CompanyName</span></span>
<span data-ttu-id="d97e2-123">Şirketin adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-123">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="d97e2-124">-ContactPerson</span></span>
<span data-ttu-id="d97e2-125">Kişi adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-125">Name of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-126">-Ülke</span><span class="sxs-lookup"><span data-stu-id="d97e2-126">-Country</span></span>
<span data-ttu-id="d97e2-127">Ülkenin adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-127">Name of the Country</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97e2-128">-DefaultProfile</span></span>
<span data-ttu-id="d97e2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d97e2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97e2-130">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="d97e2-130">-DeviceName</span></span>
<span data-ttu-id="d97e2-131">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-131">Resource Name</span></span>

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

### <span data-ttu-id="d97e2-132">-E-posta</span><span class="sxs-lookup"><span data-stu-id="d97e2-132">-Email</span></span>
<span data-ttu-id="d97e2-133">E-postaların listesi</span><span class="sxs-lookup"><span data-stu-id="d97e2-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="d97e2-134">-Phone</span></span>
<span data-ttu-id="d97e2-135">İlgili kişinin telefon numarası</span><span class="sxs-lookup"><span data-stu-id="d97e2-135">Phone number of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-136">-PostaKodu</span><span class="sxs-lookup"><span data-stu-id="d97e2-136">-PostalCode</span></span>
<span data-ttu-id="d97e2-137">Adresin posta kodu</span><span class="sxs-lookup"><span data-stu-id="d97e2-137">Postal Code of the Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97e2-138">-ResourceGroupName</span></span>
<span data-ttu-id="d97e2-139">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-139">Resource Group Name</span></span>

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

### <span data-ttu-id="d97e2-140">Durumlu</span><span class="sxs-lookup"><span data-stu-id="d97e2-140">-State</span></span>
<span data-ttu-id="d97e2-141">Eyalet adı</span><span class="sxs-lookup"><span data-stu-id="d97e2-141">Name of the State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d97e2-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d97e2-142">-Confirm</span></span>
<span data-ttu-id="d97e2-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d97e2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97e2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97e2-144">-WhatIf</span></span>
<span data-ttu-id="d97e2-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d97e2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d97e2-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d97e2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97e2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97e2-147">CommonParameters</span></span>
<span data-ttu-id="d97e2-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d97e2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97e2-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d97e2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97e2-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d97e2-150">INPUTS</span></span>

### <span data-ttu-id="d97e2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d97e2-151">System.String</span></span>

## <span data-ttu-id="d97e2-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d97e2-152">OUTPUTS</span></span>

### <span data-ttu-id="d97e2-153">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d97e2-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="d97e2-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d97e2-154">NOTES</span></span>

## <span data-ttu-id="d97e2-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d97e2-155">RELATED LINKS</span></span>
