---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f2d7c10e29209870d4aa6e5176731b07f7695aff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936702"
---
# <span data-ttu-id="f533d-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="f533d-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="f533d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f533d-102">SYNOPSIS</span></span>
<span data-ttu-id="f533d-103">Bu IotHub 'in taşıyabileceği tüm geçerli SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="f533d-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="f533d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f533d-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f533d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f533d-105">DESCRIPTION</span></span>
<span data-ttu-id="f533d-106">Bu IotHub 'in taşıyabileceği tüm geçerli STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="f533d-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="f533d-107">IotHub, ücretsiz ve ücretli STB 'ler arasında geçiş yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="f533d-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="f533d-108">Bunu yapmak için iothub silmeli ve yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f533d-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="f533d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f533d-109">EXAMPLES</span></span>

### <span data-ttu-id="f533d-110">Örnek 1 geçerli STB 'leri alın</span><span class="sxs-lookup"><span data-stu-id="f533d-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f533d-111">"Myiothub" adındaki IotHub için tüm SKU 'ların listesini alır</span><span class="sxs-lookup"><span data-stu-id="f533d-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f533d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f533d-112">PARAMETERS</span></span>

### <span data-ttu-id="f533d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f533d-113">-DefaultProfile</span></span>
<span data-ttu-id="f533d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f533d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f533d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f533d-115">-Name</span></span>
<span data-ttu-id="f533d-116">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="f533d-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f533d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f533d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f533d-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f533d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f533d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f533d-119">CommonParameters</span></span>
<span data-ttu-id="f533d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f533d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f533d-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f533d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f533d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f533d-122">INPUTS</span></span>

### <span data-ttu-id="f533d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f533d-123">System.String</span></span>

## <span data-ttu-id="f533d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f533d-124">OUTPUTS</span></span>

### <span data-ttu-id="f533d-125">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubskudescription</span><span class="sxs-lookup"><span data-stu-id="f533d-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="f533d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f533d-126">NOTES</span></span>

## <span data-ttu-id="f533d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f533d-127">RELATED LINKS</span></span>
