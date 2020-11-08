---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 166dbf5520531ec5a77fbc1e7017738d7201f664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932643"
---
# <span data-ttu-id="a5a08-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="a5a08-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="a5a08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a08-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a08-103">Desteklenen geçiş Işlemlerini Listele</span><span class="sxs-lookup"><span data-stu-id="a5a08-103">List supported Relay Operations</span></span>

## <span data-ttu-id="a5a08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5a08-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5a08-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a08-106">**Get-AzRelayOperation** cmdlet 'ı, geçiş desteklenen işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="a5a08-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="a5a08-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5a08-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a08-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5a08-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="a5a08-109">Geçiş destekli işlemleri listeler</span><span class="sxs-lookup"><span data-stu-id="a5a08-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="a5a08-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5a08-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a08-111">-DefaultProfile</span></span>
<span data-ttu-id="a5a08-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5a08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a08-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a08-113">CommonParameters</span></span>
<span data-ttu-id="a5a08-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5a08-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a08-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a08-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a08-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5a08-116">INPUTS</span></span>

### <span data-ttu-id="a5a08-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a5a08-117">None</span></span>

## <span data-ttu-id="a5a08-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5a08-118">OUTPUTS</span></span>

### <span data-ttu-id="a5a08-119">Microsoft. Azure. Commands. Relay. model. Psoperationöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="a5a08-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="a5a08-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5a08-120">NOTES</span></span>

## <span data-ttu-id="a5a08-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5a08-121">RELATED LINKS</span></span>