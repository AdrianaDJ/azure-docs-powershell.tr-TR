---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 49b47e637d009eabac106679e81ec763b0898160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936720"
---
# <span data-ttu-id="a9557-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="a9557-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="a9557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9557-102">SYNOPSIS</span></span>
<span data-ttu-id="a9557-103">Verilen ad alanı adının veya diğer adın uygunluk durumunu denetler (DR yapılandırma adı)</span><span class="sxs-lookup"><span data-stu-id="a9557-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a9557-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9557-104">SYNTAX</span></span>

### <span data-ttu-id="a9557-105">Namespacechecknamekullanılabilirliği Bilityset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9557-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9557-106">Diğerad</span><span class="sxs-lookup"><span data-stu-id="a9557-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9557-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9557-107">DESCRIPTION</span></span>
<span data-ttu-id="a9557-108">**Test-AzEventhubName** cmdlet 'ı ad alanı adının veya diğer adın kullanılabilirliğini DENETLER (Dr yapılandırma adı)</span><span class="sxs-lookup"><span data-stu-id="a9557-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a9557-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9557-109">EXAMPLES</span></span>

### <span data-ttu-id="a9557-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9557-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a9557-111">Kullanılabiliyorsa, ' MyNameSapceName ' ad alanı adının kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="a9557-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="a9557-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9557-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a9557-113">' MyNameSapceName ' ad alanı adının kullanılabilirliği nedeniyle durumu yanlış olarak verir</span><span class="sxs-lookup"><span data-stu-id="a9557-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a9557-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a9557-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="a9557-115">Varsa, ' MyNameSapceName ' ad alanı için ' myAliasName ' ad alanı kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="a9557-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="a9557-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9557-116">PARAMETERS</span></span>

### <span data-ttu-id="a9557-117">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="a9557-117">-AliasName</span></span>
<span data-ttu-id="a9557-118">DR yapılandırma adı-diğer ad</span><span class="sxs-lookup"><span data-stu-id="a9557-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="a9557-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9557-119">-DefaultProfile</span></span>
<span data-ttu-id="a9557-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9557-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9557-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9557-121">-Namespace</span></span>
<span data-ttu-id="a9557-122">Eventhub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a9557-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="a9557-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9557-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9557-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a9557-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9557-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9557-125">CommonParameters</span></span>
<span data-ttu-id="a9557-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9557-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9557-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9557-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9557-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9557-128">INPUTS</span></span>

### <span data-ttu-id="a9557-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a9557-129">System.String</span></span>

## <span data-ttu-id="a9557-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9557-130">OUTPUTS</span></span>

### <span data-ttu-id="a9557-131">Microsoft. Azure. Commands. EventHub. model. Pschecknamekullanılabilirliği Bilityresultattributes</span><span class="sxs-lookup"><span data-stu-id="a9557-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="a9557-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9557-132">NOTES</span></span>

## <span data-ttu-id="a9557-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9557-133">RELATED LINKS</span></span>