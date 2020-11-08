---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280273"
---
# <span data-ttu-id="fd7fb-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="fd7fb-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="fd7fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7fb-103">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="fd7fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd7fb-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd7fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd7fb-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7fb-106">Bir IotHub için RegistryStatistics 'i alır.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="fd7fb-107">Bu, IotHub içindeki toplam etkin ve devre dışı aygıtların sayısı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="fd7fb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd7fb-108">EXAMPLES</span></span>

### <span data-ttu-id="fd7fb-109">Örnek 1 RegistryStatistics 'i alma</span><span class="sxs-lookup"><span data-stu-id="fd7fb-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fd7fb-110">"Myiothub" adındaki IotHub için kayıt</span><span class="sxs-lookup"><span data-stu-id="fd7fb-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fd7fb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd7fb-111">PARAMETERS</span></span>

### <span data-ttu-id="fd7fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7fb-112">-DefaultProfile</span></span>
<span data-ttu-id="fd7fb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd7fb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd7fb-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd7fb-114">-Name</span></span>
<span data-ttu-id="fd7fb-115">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="fd7fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd7fb-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fd7fb-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fd7fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7fb-118">CommonParameters</span></span>
<span data-ttu-id="fd7fb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7fb-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7fb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7fb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd7fb-121">INPUTS</span></span>

### <span data-ttu-id="fd7fb-122">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7fb-122">System.String</span></span>

## <span data-ttu-id="fd7fb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd7fb-123">OUTPUTS</span></span>

### <span data-ttu-id="fd7fb-124">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubregistrystatistics</span><span class="sxs-lookup"><span data-stu-id="fd7fb-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="fd7fb-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd7fb-125">NOTES</span></span>

## <span data-ttu-id="fd7fb-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd7fb-126">RELATED LINKS</span></span>
