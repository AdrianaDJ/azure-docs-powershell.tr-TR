---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: fbbac617687712208730393b978a3df5b404aeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590629"
---
# <span data-ttu-id="22acb-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="22acb-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="22acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22acb-102">SYNOPSIS</span></span>
<span data-ttu-id="22acb-103">Desteklenen ServiceBus Işlemlerini Listele</span><span class="sxs-lookup"><span data-stu-id="22acb-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22acb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22acb-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22acb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22acb-105">DESCRIPTION</span></span>
<span data-ttu-id="22acb-106">**Get-AzureRmServiceBusOperation** cmdlet 'ı, ServiceBus desteklenen işlemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="22acb-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="22acb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22acb-107">EXAMPLES</span></span>

### <span data-ttu-id="22acb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22acb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="22acb-109">ServiceBus desteklenen işlemleri listeler</span><span class="sxs-lookup"><span data-stu-id="22acb-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="22acb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22acb-110">PARAMETERS</span></span>

### <span data-ttu-id="22acb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22acb-111">-DefaultProfile</span></span>
<span data-ttu-id="22acb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22acb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22acb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22acb-113">CommonParameters</span></span>
<span data-ttu-id="22acb-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22acb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22acb-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22acb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22acb-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22acb-116">INPUTS</span></span>

### <span data-ttu-id="22acb-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="22acb-117">None</span></span>

### <span data-ttu-id="22acb-118">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. OperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22acb-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22acb-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22acb-119">OUTPUTS</span></span>

### <span data-ttu-id="22acb-120">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ServiceBus. model. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="22acb-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="22acb-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22acb-121">NOTES</span></span>

## <span data-ttu-id="22acb-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22acb-122">RELATED LINKS</span></span>

