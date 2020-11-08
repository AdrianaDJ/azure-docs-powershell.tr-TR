---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938137"
---
# <span data-ttu-id="97a68-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="97a68-101">Test-AzRelayName</span></span>

## <span data-ttu-id="97a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a68-102">SYNOPSIS</span></span>
<span data-ttu-id="97a68-103">Verilen ad alanı adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="97a68-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="97a68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97a68-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a68-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97a68-105">DESCRIPTION</span></span>
<span data-ttu-id="97a68-106">**Test-AzRelayName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler</span><span class="sxs-lookup"><span data-stu-id="97a68-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="97a68-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97a68-107">EXAMPLES</span></span>

### <span data-ttu-id="97a68-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97a68-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="97a68-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="97a68-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="97a68-110">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="97a68-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="97a68-111">Ad alanı adının uygunluk durumunu verir</span><span class="sxs-lookup"><span data-stu-id="97a68-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="97a68-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97a68-112">PARAMETERS</span></span>

### <span data-ttu-id="97a68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a68-113">-DefaultProfile</span></span>
<span data-ttu-id="97a68-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97a68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a68-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="97a68-115">-Namespace</span></span>
<span data-ttu-id="97a68-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="97a68-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="97a68-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a68-117">CommonParameters</span></span>
<span data-ttu-id="97a68-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97a68-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a68-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a68-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a68-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97a68-120">INPUTS</span></span>

### <span data-ttu-id="97a68-121">System. String</span><span class="sxs-lookup"><span data-stu-id="97a68-121">System.String</span></span>

## <span data-ttu-id="97a68-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97a68-122">OUTPUTS</span></span>

### <span data-ttu-id="97a68-123">Microsoft. Azure. Commands. Relay. model. Pschecknamekullanılabilirliği Bilityresultattributes</span><span class="sxs-lookup"><span data-stu-id="97a68-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="97a68-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97a68-124">NOTES</span></span>

## <span data-ttu-id="97a68-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97a68-125">RELATED LINKS</span></span>