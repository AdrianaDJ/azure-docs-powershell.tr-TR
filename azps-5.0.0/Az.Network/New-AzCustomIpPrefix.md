---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278549"
---
# <span data-ttu-id="94f5a-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="94f5a-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="94f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="94f5a-103">Custobir önek kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="94f5a-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="94f5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94f5a-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94f5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="94f5a-106">**New-Azcustoi önek** cmdlet 'ı bir custobir önek kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94f5a-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="94f5a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="94f5a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94f5a-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="94f5a-109">Bu komut, westus 'da CIDR 40.40.40.0/24 içeren kaynak grubunda ad $prefixName olan yeni bir özelmi önek kaynağı oluşturur $rgName</span><span class="sxs-lookup"><span data-stu-id="94f5a-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="94f5a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94f5a-110">PARAMETERS</span></span>

### <span data-ttu-id="94f5a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="94f5a-111">-AsJob</span></span>
<span data-ttu-id="94f5a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="94f5a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f5a-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="94f5a-113">-Cidr</span></span>
<span data-ttu-id="94f5a-114">Özelmi, CıDR öneki.</span><span class="sxs-lookup"><span data-stu-id="94f5a-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f5a-115">-DefaultProfile</span></span>
<span data-ttu-id="94f5a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94f5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="94f5a-117">-Location</span></span>
<span data-ttu-id="94f5a-118">Özelmi önek konumu.</span><span class="sxs-lookup"><span data-stu-id="94f5a-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="94f5a-119">-Name</span></span>
<span data-ttu-id="94f5a-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="94f5a-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="94f5a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="94f5a-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="94f5a-123">-Tag</span></span>
<span data-ttu-id="94f5a-124">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="94f5a-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-125">-Bölge</span><span class="sxs-lookup"><span data-stu-id="94f5a-125">-Zone</span></span>
<span data-ttu-id="94f5a-126">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="94f5a-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="94f5a-127">-Confirm</span></span>
<span data-ttu-id="94f5a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94f5a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f5a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f5a-129">-WhatIf</span></span>
<span data-ttu-id="94f5a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94f5a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f5a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94f5a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f5a-132">CommonParameters</span></span>
<span data-ttu-id="94f5a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94f5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f5a-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94f5a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f5a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94f5a-135">INPUTS</span></span>

### <span data-ttu-id="94f5a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="94f5a-136">System.String</span></span>

### <span data-ttu-id="94f5a-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="94f5a-137">System.String[]</span></span>

### <span data-ttu-id="94f5a-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94f5a-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94f5a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94f5a-139">OUTPUTS</span></span>

### <span data-ttu-id="94f5a-140">Microsoft. Azure. Commands. Network. model. Pscustolermi öneki</span><span class="sxs-lookup"><span data-stu-id="94f5a-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="94f5a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94f5a-141">NOTES</span></span>

## <span data-ttu-id="94f5a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94f5a-142">RELATED LINKS</span></span>

[<span data-ttu-id="94f5a-143">Get-Azözelmi öneki</span><span class="sxs-lookup"><span data-stu-id="94f5a-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="94f5a-144">Remove-Azcustomhttp öneki</span><span class="sxs-lookup"><span data-stu-id="94f5a-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="94f5a-145">Update-Azcustombu önek</span><span class="sxs-lookup"><span data-stu-id="94f5a-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)