---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587800"
---
# <span data-ttu-id="cd618-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cd618-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="cd618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd618-102">SYNOPSIS</span></span>
<span data-ttu-id="cd618-103">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="cd618-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd618-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd618-104">SYNTAX</span></span>

### <span data-ttu-id="cd618-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd618-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd618-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd618-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd618-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="cd618-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd618-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd618-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd618-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd618-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd618-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd618-110">DESCRIPTION</span></span>
<span data-ttu-id="cd618-111">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="cd618-111">Filters active directory users.</span></span>

## <span data-ttu-id="cd618-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd618-112">EXAMPLES</span></span>

### <span data-ttu-id="cd618-113">--------------------------Kullanıcılara UPN--------------------------kullanarak filtre uygular</span><span class="sxs-lookup"><span data-stu-id="cd618-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="cd618-114">Kullanıcıyı ile alır foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="cd618-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="cd618-115">--------------------------Arama dizesi kullanarak kullanıcıları filtreler--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd618-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="cd618-116">Görünen adında Joe içeren tüm ad kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="cd618-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="cd618-117">----------------------------------------------------Liste</span><span class="sxs-lookup"><span data-stu-id="cd618-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="cd618-118">Tüm reklam kullanıcılarını alır</span><span class="sxs-lookup"><span data-stu-id="cd618-118">Gets all AD users</span></span>

## <span data-ttu-id="cd618-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd618-119">PARAMETERS</span></span>

### <span data-ttu-id="cd618-120">-Posta</span><span class="sxs-lookup"><span data-stu-id="cd618-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd618-121">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="cd618-121">-ObjectId</span></span>
<span data-ttu-id="cd618-122">Kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="cd618-122">Object id of the user.</span></span>

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

### <span data-ttu-id="cd618-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="cd618-123">-SearchString</span></span>
<span data-ttu-id="cd618-124">Kullanıcının görünen adı</span><span class="sxs-lookup"><span data-stu-id="cd618-124">The user display name</span></span>

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

### <span data-ttu-id="cd618-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cd618-125">-UserPrincipalName</span></span>
<span data-ttu-id="cd618-126">Kullanıcının UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="cd618-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd618-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd618-127">-DefaultProfile</span></span>
<span data-ttu-id="cd618-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd618-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd618-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd618-129">CommonParameters</span></span>
<span data-ttu-id="cd618-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd618-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd618-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd618-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd618-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd618-132">INPUTS</span></span>

## <span data-ttu-id="cd618-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd618-133">OUTPUTS</span></span>

### <span data-ttu-id="cd618-134">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="cd618-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="cd618-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd618-135">NOTES</span></span>

## <span data-ttu-id="cd618-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd618-136">RELATED LINKS</span></span>

[<span data-ttu-id="cd618-137">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cd618-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="cd618-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cd618-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="cd618-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cd618-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

