---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595014"
---
# <span data-ttu-id="24d75-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="24d75-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="24d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d75-102">SYNOPSIS</span></span>
<span data-ttu-id="24d75-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24d75-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24d75-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24d75-105">DESCRIPTION</span></span>
<span data-ttu-id="24d75-106">**Yeni-AzureRmAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24d75-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="24d75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24d75-107">EXAMPLES</span></span>

### <span data-ttu-id="24d75-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="24d75-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="24d75-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailablitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24d75-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="24d75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24d75-110">PARAMETERS</span></span>

### <span data-ttu-id="24d75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d75-111">-DefaultProfile</span></span>
<span data-ttu-id="24d75-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24d75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="24d75-113">-Location</span></span>
<span data-ttu-id="24d75-114">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="24d75-114">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="24d75-115">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="24d75-115">-Managed</span></span>
<span data-ttu-id="24d75-116">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="24d75-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="24d75-117">-Name</span></span>
<span data-ttu-id="24d75-118">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="24d75-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="24d75-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="24d75-120">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24d75-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="24d75-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="24d75-122">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24d75-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d75-123">-ResourceGroupName</span></span>
<span data-ttu-id="24d75-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24d75-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="24d75-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="24d75-125">-Sku</span></span>
<span data-ttu-id="24d75-126">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="24d75-126">The Name of Sku</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d75-127">CommonParameters</span></span>
<span data-ttu-id="24d75-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24d75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d75-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d75-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d75-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24d75-130">INPUTS</span></span>

## <span data-ttu-id="24d75-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24d75-131">OUTPUTS</span></span>

## <span data-ttu-id="24d75-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24d75-132">NOTES</span></span>

## <span data-ttu-id="24d75-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24d75-133">RELATED LINKS</span></span>

[<span data-ttu-id="24d75-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="24d75-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="24d75-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="24d75-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


