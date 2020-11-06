---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589126"
---
# <span data-ttu-id="a7eed-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="a7eed-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="a7eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7eed-102">SYNOPSIS</span></span>
<span data-ttu-id="a7eed-103">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="a7eed-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7eed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7eed-104">SYNTAX</span></span>

### <span data-ttu-id="a7eed-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7eed-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7eed-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7eed-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7eed-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="a7eed-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7eed-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7eed-108">DESCRIPTION</span></span>
<span data-ttu-id="a7eed-109">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="a7eed-109">Filters active directory groups.</span></span>

## <span data-ttu-id="a7eed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7eed-110">EXAMPLES</span></span>

### <span data-ttu-id="a7eed-111">--------------------------, Nesne kimliğini kullanarak gruplar--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7eed-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="a7eed-112">85 f89c90-780e-4aa6-9F</span><span class="sxs-lookup"><span data-stu-id="a7eed-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="a7eed-113">--------------------------Arama dizesi kullanarak gruplar--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7eed-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="a7eed-114">Ekran adında Joe içeren tüm ad gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="a7eed-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="a7eed-115">--------------------------Liste grupları--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7eed-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="a7eed-116">Tüm AD gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="a7eed-116">Gets all AD groups</span></span>

## <span data-ttu-id="a7eed-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7eed-117">PARAMETERS</span></span>

### <span data-ttu-id="a7eed-118">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a7eed-118">-ObjectId</span></span>
<span data-ttu-id="a7eed-119">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="a7eed-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eed-120">-SearchString</span><span class="sxs-lookup"><span data-stu-id="a7eed-120">-SearchString</span></span>
<span data-ttu-id="a7eed-121">Grup görünen adı</span><span class="sxs-lookup"><span data-stu-id="a7eed-121">The group display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7eed-122">-DefaultProfile</span></span>
<span data-ttu-id="a7eed-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7eed-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7eed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7eed-124">CommonParameters</span></span>
<span data-ttu-id="a7eed-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7eed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7eed-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7eed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7eed-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7eed-127">INPUTS</span></span>

## <span data-ttu-id="a7eed-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7eed-128">OUTPUTS</span></span>

### <span data-ttu-id="a7eed-129">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="a7eed-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="a7eed-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7eed-130">NOTES</span></span>

## <span data-ttu-id="a7eed-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7eed-131">RELATED LINKS</span></span>

[<span data-ttu-id="a7eed-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a7eed-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="a7eed-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a7eed-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a7eed-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="a7eed-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

