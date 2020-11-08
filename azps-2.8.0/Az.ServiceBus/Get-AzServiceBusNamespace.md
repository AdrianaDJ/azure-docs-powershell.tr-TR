---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: db18a260e86431d60c8fb0722d8276982eec8275
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933246"
---
# <span data-ttu-id="39498-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="39498-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="39498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39498-102">SYNOPSIS</span></span>
<span data-ttu-id="39498-103">Kaynak grubunda belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="39498-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="39498-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39498-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39498-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39498-105">DESCRIPTION</span></span>
<span data-ttu-id="39498-106">**Get-AzServiceBusNamespace** cmdlet 'i, kaynak grubundaki belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="39498-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="39498-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39498-107">EXAMPLES</span></span>

### <span data-ttu-id="39498-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39498-108">Example 1</span></span>

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

## <span data-ttu-id="39498-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39498-109">PARAMETERS</span></span>

### <span data-ttu-id="39498-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39498-110">-DefaultProfile</span></span>
<span data-ttu-id="39498-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39498-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39498-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="39498-112">-Name</span></span>
<span data-ttu-id="39498-113">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="39498-113">Namespace Name.</span></span>

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

### <span data-ttu-id="39498-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39498-114">-ResourceGroupName</span></span>
<span data-ttu-id="39498-115">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="39498-115">The name of the resource group</span></span>

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

### <span data-ttu-id="39498-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39498-116">CommonParameters</span></span>
<span data-ttu-id="39498-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39498-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39498-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39498-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39498-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39498-119">INPUTS</span></span>

### <span data-ttu-id="39498-120">System. String</span><span class="sxs-lookup"><span data-stu-id="39498-120">System.String</span></span>

## <span data-ttu-id="39498-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39498-121">OUTPUTS</span></span>

### <span data-ttu-id="39498-122">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="39498-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="39498-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39498-123">NOTES</span></span>

## <span data-ttu-id="39498-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39498-124">RELATED LINKS</span></span>