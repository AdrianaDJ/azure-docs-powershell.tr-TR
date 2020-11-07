---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763236"
---
# <span data-ttu-id="c8238-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c8238-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="c8238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8238-102">SYNOPSIS</span></span>
<span data-ttu-id="c8238-103">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="c8238-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8238-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8238-104">SYNTAX</span></span>

### <span data-ttu-id="c8238-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8238-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8238-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8238-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8238-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="c8238-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8238-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8238-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8238-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8238-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8238-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8238-110">DESCRIPTION</span></span>
<span data-ttu-id="c8238-111">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="c8238-111">Filters active directory users.</span></span>

## <span data-ttu-id="c8238-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8238-112">EXAMPLES</span></span>

### <span data-ttu-id="c8238-113">UPN kullanan kullanıcıları filtreler</span><span class="sxs-lookup"><span data-stu-id="c8238-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="c8238-114">Kullanıcıyı ile alır foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="c8238-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="c8238-115">Arama dizesini kullanan kullanıcıları filtreler</span><span class="sxs-lookup"><span data-stu-id="c8238-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="c8238-116">Görünen adında Joe içeren tüm ad kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="c8238-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="c8238-117">Liste</span><span class="sxs-lookup"><span data-stu-id="c8238-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="c8238-118">Tüm reklam kullanıcılarını alır</span><span class="sxs-lookup"><span data-stu-id="c8238-118">Gets all AD users</span></span>

## <span data-ttu-id="c8238-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8238-119">PARAMETERS</span></span>

### <span data-ttu-id="c8238-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8238-120">-DefaultProfile</span></span>
<span data-ttu-id="c8238-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8238-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8238-122">-Posta</span><span class="sxs-lookup"><span data-stu-id="c8238-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8238-123">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c8238-123">-ObjectId</span></span>
<span data-ttu-id="c8238-124">Kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8238-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8238-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="c8238-125">-SearchString</span></span>
<span data-ttu-id="c8238-126">Kullanıcının görünen adı</span><span class="sxs-lookup"><span data-stu-id="c8238-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8238-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c8238-127">-UserPrincipalName</span></span>
<span data-ttu-id="c8238-128">Kullanıcının UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="c8238-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8238-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8238-129">CommonParameters</span></span>
<span data-ttu-id="c8238-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8238-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8238-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8238-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8238-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8238-132">INPUTS</span></span>

### <span data-ttu-id="c8238-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8238-133">None</span></span>
<span data-ttu-id="c8238-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c8238-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8238-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8238-135">OUTPUTS</span></span>

### <span data-ttu-id="c8238-136">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="c8238-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="c8238-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8238-137">NOTES</span></span>

## <span data-ttu-id="c8238-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8238-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8238-139">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c8238-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="c8238-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c8238-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="c8238-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c8238-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

