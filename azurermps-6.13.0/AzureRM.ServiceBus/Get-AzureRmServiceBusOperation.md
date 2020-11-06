---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: e70ff7da7c005f6376d3c4e7a6aae5295e53f693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591906"
---
# <span data-ttu-id="f5aa5-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="f5aa5-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="f5aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="f5aa5-103">Desteklenen ServiceBus Işlemlerini Listele</span><span class="sxs-lookup"><span data-stu-id="f5aa5-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5aa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5aa5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="f5aa5-106">**Get-AzureRmServiceBusOperation** cmdlet 'ı, ServiceBus desteklenen işlemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="f5aa5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="f5aa5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5aa5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="f5aa5-109">ServiceBus desteklenen işlemleri listeler</span><span class="sxs-lookup"><span data-stu-id="f5aa5-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="f5aa5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5aa5-110">PARAMETERS</span></span>

### <span data-ttu-id="f5aa5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5aa5-111">-DefaultProfile</span></span>
<span data-ttu-id="f5aa5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5aa5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5aa5-113">CommonParameters</span></span>
<span data-ttu-id="f5aa5-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5aa5-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5aa5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5aa5-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-116">INPUTS</span></span>

### <span data-ttu-id="f5aa5-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f5aa5-117">None</span></span>

## <span data-ttu-id="f5aa5-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5aa5-118">OUTPUTS</span></span>

### <span data-ttu-id="f5aa5-119">Microsoft. Azure. Commands. ServiceBus. model. Psoperationöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="f5aa5-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="f5aa5-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5aa5-120">NOTES</span></span>

## <span data-ttu-id="f5aa5-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5aa5-121">RELATED LINKS</span></span>
