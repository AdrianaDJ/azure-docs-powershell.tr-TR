---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763993"
---
# <span data-ttu-id="2065a-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="2065a-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="2065a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2065a-102">SYNOPSIS</span></span>
<span data-ttu-id="2065a-103">Desteklenen ServiceBus Işlemlerini Listele</span><span class="sxs-lookup"><span data-stu-id="2065a-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2065a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2065a-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2065a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2065a-105">DESCRIPTION</span></span>
<span data-ttu-id="2065a-106">**Get-AzureRmServiceBusOperation** cmdlet 'ı, ServiceBus desteklenen işlemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="2065a-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="2065a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2065a-107">EXAMPLES</span></span>

### <span data-ttu-id="2065a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2065a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="2065a-109">ServiceBus desteklenen işlemleri listeler</span><span class="sxs-lookup"><span data-stu-id="2065a-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="2065a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2065a-110">PARAMETERS</span></span>

### <span data-ttu-id="2065a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2065a-111">-DefaultProfile</span></span>
<span data-ttu-id="2065a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2065a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2065a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2065a-113">CommonParameters</span></span>
<span data-ttu-id="2065a-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2065a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2065a-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2065a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2065a-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2065a-116">INPUTS</span></span>

### <span data-ttu-id="2065a-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2065a-117">None</span></span>

### <span data-ttu-id="2065a-118">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. PSOperationAttributes, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2065a-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2065a-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2065a-119">OUTPUTS</span></span>

### <span data-ttu-id="2065a-120">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ServiceBus. model. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="2065a-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="2065a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2065a-121">NOTES</span></span>

## <span data-ttu-id="2065a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2065a-122">RELATED LINKS</span></span>

