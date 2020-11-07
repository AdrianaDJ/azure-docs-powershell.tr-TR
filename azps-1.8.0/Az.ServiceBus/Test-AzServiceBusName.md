---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759130"
---
# <span data-ttu-id="b006a-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="b006a-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="b006a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b006a-102">SYNOPSIS</span></span>
<span data-ttu-id="b006a-103">Verilen ad alanı adının veya diğer adın uygunluk durumunu denetler (DR yapılandırma adı)</span><span class="sxs-lookup"><span data-stu-id="b006a-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="b006a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b006a-104">SYNTAX</span></span>

### <span data-ttu-id="b006a-105">Diğerad</span><span class="sxs-lookup"><span data-stu-id="b006a-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b006a-106">Namespacechecknamekullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="b006a-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b006a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b006a-107">DESCRIPTION</span></span>
<span data-ttu-id="b006a-108">**Test-Azhizmetibusname** cmdlet 'ı ad alanı adının veya diğer adının kullanılabilirliğini denetleme (Dr yapılandırma adı)</span><span class="sxs-lookup"><span data-stu-id="b006a-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="b006a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b006a-109">EXAMPLES</span></span>

### <span data-ttu-id="b006a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b006a-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="b006a-111">' MyNameSapceName ' ad alanı adının kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="b006a-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="b006a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b006a-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="b006a-113">' MyNameSapceName ' ad alanı adının kullanılabilirliği nedeniyle durumu yanlış olarak verir</span><span class="sxs-lookup"><span data-stu-id="b006a-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="b006a-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b006a-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="b006a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b006a-115">PARAMETERS</span></span>

### <span data-ttu-id="b006a-116">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="b006a-116">-AliasName</span></span>
<span data-ttu-id="b006a-117">DR yapılandırma adı-diğer ad</span><span class="sxs-lookup"><span data-stu-id="b006a-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b006a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b006a-118">-DefaultProfile</span></span>
<span data-ttu-id="b006a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b006a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b006a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b006a-120">-Namespace</span></span>
<span data-ttu-id="b006a-121">ServiceBus ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b006a-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b006a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b006a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b006a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b006a-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b006a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b006a-124">CommonParameters</span></span>
<span data-ttu-id="b006a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b006a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b006a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b006a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b006a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b006a-127">INPUTS</span></span>

### <span data-ttu-id="b006a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b006a-128">System.String</span></span>

## <span data-ttu-id="b006a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b006a-129">OUTPUTS</span></span>

### <span data-ttu-id="b006a-130">Microsoft. Azure. Commands. ServiceBus. modeller. Pschecknamekullanılabilirliği Bilityresultattributes</span><span class="sxs-lookup"><span data-stu-id="b006a-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="b006a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b006a-131">NOTES</span></span>

## <span data-ttu-id="b006a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b006a-132">RELATED LINKS</span></span>