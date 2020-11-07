---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938990"
---
# <span data-ttu-id="6927b-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6927b-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="6927b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6927b-102">SYNOPSIS</span></span>
<span data-ttu-id="6927b-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6927b-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6927b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6927b-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6927b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6927b-105">DESCRIPTION</span></span>
<span data-ttu-id="6927b-106">**Yeni-AzureRmAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6927b-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="6927b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6927b-107">EXAMPLES</span></span>

### <span data-ttu-id="6927b-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6927b-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="6927b-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailablitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6927b-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="6927b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6927b-110">PARAMETERS</span></span>

### <span data-ttu-id="6927b-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="6927b-111">-AsJob</span></span>
<span data-ttu-id="6927b-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="6927b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6927b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6927b-113">-DefaultProfile</span></span>
<span data-ttu-id="6927b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6927b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6927b-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6927b-115">-Location</span></span>
<span data-ttu-id="6927b-116">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6927b-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="6927b-117">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="6927b-117">-Managed</span></span>
<span data-ttu-id="6927b-118">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="6927b-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="6927b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6927b-119">-Name</span></span>
<span data-ttu-id="6927b-120">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6927b-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="6927b-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="6927b-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="6927b-122">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6927b-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="6927b-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="6927b-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="6927b-124">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6927b-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="6927b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6927b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6927b-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6927b-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6927b-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="6927b-127">-Sku</span></span>
<span data-ttu-id="6927b-128">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="6927b-128">The Name of Sku</span></span>
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

### <span data-ttu-id="6927b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6927b-129">CommonParameters</span></span>
<span data-ttu-id="6927b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6927b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6927b-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6927b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6927b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6927b-132">INPUTS</span></span>

### <span data-ttu-id="6927b-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6927b-133">None</span></span>
<span data-ttu-id="6927b-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6927b-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6927b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6927b-135">OUTPUTS</span></span>

### <span data-ttu-id="6927b-136">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6927b-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6927b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6927b-137">NOTES</span></span>

## <span data-ttu-id="6927b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6927b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6927b-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6927b-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="6927b-140">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6927b-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


