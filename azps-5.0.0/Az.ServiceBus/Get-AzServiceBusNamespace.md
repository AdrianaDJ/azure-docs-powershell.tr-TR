---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276547"
---
# <span data-ttu-id="9cac6-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9cac6-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="9cac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cac6-102">SYNOPSIS</span></span>
<span data-ttu-id="9cac6-103">Kaynak grubunda belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="9cac6-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="9cac6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cac6-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cac6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cac6-105">DESCRIPTION</span></span>
<span data-ttu-id="9cac6-106">**Get-AzServiceBusNamespace** cmdlet 'i, kaynak grubundaki belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="9cac6-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="9cac6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cac6-107">EXAMPLES</span></span>

### <span data-ttu-id="9cac6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cac6-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="9cac6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cac6-109">PARAMETERS</span></span>

### <span data-ttu-id="9cac6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cac6-110">-DefaultProfile</span></span>
<span data-ttu-id="9cac6-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cac6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cac6-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cac6-112">-Name</span></span>
<span data-ttu-id="9cac6-113">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9cac6-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cac6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cac6-114">-ResourceGroupName</span></span>
<span data-ttu-id="9cac6-115">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9cac6-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cac6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cac6-116">CommonParameters</span></span>
<span data-ttu-id="9cac6-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cac6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cac6-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cac6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cac6-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cac6-119">INPUTS</span></span>

### <span data-ttu-id="9cac6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9cac6-120">System.String</span></span>

## <span data-ttu-id="9cac6-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cac6-121">OUTPUTS</span></span>

### <span data-ttu-id="9cac6-122">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9cac6-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9cac6-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cac6-123">NOTES</span></span>

## <span data-ttu-id="9cac6-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cac6-124">RELATED LINKS</span></span>
