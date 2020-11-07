---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f81419f43defdf2c66d2d8f1768c63fc09ff0d35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916444"
---
# <span data-ttu-id="b9089-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="b9089-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="b9089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9089-102">SYNOPSIS</span></span>
<span data-ttu-id="b9089-103">Bu IotHub 'in taşıyabileceği tüm geçerli SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="b9089-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="b9089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9089-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9089-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9089-105">DESCRIPTION</span></span>
<span data-ttu-id="b9089-106">Bu IotHub 'in taşıyabileceği tüm geçerli STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="b9089-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="b9089-107">IotHub, ücretsiz ve ücretli STB 'ler arasında geçiş yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="b9089-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="b9089-108">Bunu yapmak için iothub silmeli ve yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="b9089-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="b9089-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9089-109">EXAMPLES</span></span>

### <span data-ttu-id="b9089-110">Örnek 1 geçerli STB 'leri alın</span><span class="sxs-lookup"><span data-stu-id="b9089-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b9089-111">"Myiothub" adındaki IotHub için tüm SKU 'ların listesini alır</span><span class="sxs-lookup"><span data-stu-id="b9089-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b9089-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9089-112">PARAMETERS</span></span>

### <span data-ttu-id="b9089-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9089-113">-DefaultProfile</span></span>
<span data-ttu-id="b9089-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b9089-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9089-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9089-115">-Name</span></span>
<span data-ttu-id="b9089-116">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="b9089-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b9089-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9089-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9089-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b9089-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b9089-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9089-119">CommonParameters</span></span>
<span data-ttu-id="b9089-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9089-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9089-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9089-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9089-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9089-122">INPUTS</span></span>

### <span data-ttu-id="b9089-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b9089-123">System.String</span></span>

## <span data-ttu-id="b9089-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9089-124">OUTPUTS</span></span>

### <span data-ttu-id="b9089-125">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubskudescription</span><span class="sxs-lookup"><span data-stu-id="b9089-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="b9089-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9089-126">NOTES</span></span>

## <span data-ttu-id="b9089-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9089-127">RELATED LINKS</span></span>
