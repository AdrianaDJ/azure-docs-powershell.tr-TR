---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763365"
---
# <span data-ttu-id="ea315-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="ea315-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="ea315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea315-102">SYNOPSIS</span></span>
<span data-ttu-id="ea315-103">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="ea315-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea315-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea315-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea315-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea315-105">DESCRIPTION</span></span>
<span data-ttu-id="ea315-106">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="ea315-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="ea315-107">Bu, IotHub içindeki toplam etkin ve devre dışı aygıtların sayısı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ea315-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="ea315-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea315-108">EXAMPLES</span></span>

### <span data-ttu-id="ea315-109">Örnek 1 RegistryStatistics 'i alma</span><span class="sxs-lookup"><span data-stu-id="ea315-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ea315-110">"Myiothub" adındaki IotHub için kayıt</span><span class="sxs-lookup"><span data-stu-id="ea315-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ea315-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea315-111">PARAMETERS</span></span>

### <span data-ttu-id="ea315-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea315-112">-Name</span></span>
<span data-ttu-id="ea315-113">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="ea315-113">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="ea315-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea315-114">-ResourceGroupName</span></span>
<span data-ttu-id="ea315-115">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ea315-115">Resource Group Name</span></span>

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

### <span data-ttu-id="ea315-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea315-116">-DefaultProfile</span></span>
<span data-ttu-id="ea315-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea315-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea315-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea315-118">CommonParameters</span></span>
<span data-ttu-id="ea315-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea315-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea315-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea315-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea315-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea315-121">INPUTS</span></span>

### <span data-ttu-id="ea315-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ea315-122">System.String</span></span>

## <span data-ttu-id="ea315-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea315-123">OUTPUTS</span></span>

### <span data-ttu-id="ea315-124">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubregistrystatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ea315-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea315-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea315-125">NOTES</span></span>

## <span data-ttu-id="ea315-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea315-126">RELATED LINKS</span></span>
