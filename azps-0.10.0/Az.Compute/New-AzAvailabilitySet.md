---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936981"
---
# <span data-ttu-id="a9273-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9273-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="a9273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9273-102">SYNOPSIS</span></span>
<span data-ttu-id="a9273-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9273-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="a9273-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9273-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9273-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9273-105">DESCRIPTION</span></span>
<span data-ttu-id="a9273-106">**New-AzAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9273-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="a9273-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9273-107">EXAMPLES</span></span>

### <span data-ttu-id="a9273-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9273-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="a9273-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailablitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9273-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a9273-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9273-110">PARAMETERS</span></span>

### <span data-ttu-id="a9273-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a9273-111">-AsJob</span></span>
<span data-ttu-id="a9273-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="a9273-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a9273-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9273-113">-DefaultProfile</span></span>
<span data-ttu-id="a9273-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9273-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="a9273-115">-Location</span></span>
<span data-ttu-id="a9273-116">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9273-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-117">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="a9273-117">-Managed</span></span>
<span data-ttu-id="a9273-118">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="a9273-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9273-119">-Name</span></span>
<span data-ttu-id="a9273-120">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9273-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="a9273-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="a9273-122">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9273-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="a9273-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="a9273-124">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9273-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9273-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9273-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9273-126">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9273-127">-Sku</span></span>
<span data-ttu-id="a9273-128">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="a9273-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9273-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9273-129">CommonParameters</span></span>
<span data-ttu-id="a9273-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9273-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9273-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9273-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9273-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9273-132">INPUTS</span></span>

### <span data-ttu-id="a9273-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9273-133">None</span></span>
<span data-ttu-id="a9273-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a9273-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9273-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9273-135">OUTPUTS</span></span>

### <span data-ttu-id="a9273-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9273-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="a9273-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9273-137">NOTES</span></span>

## <span data-ttu-id="a9273-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9273-138">RELATED LINKS</span></span>

[<span data-ttu-id="a9273-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9273-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a9273-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9273-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


