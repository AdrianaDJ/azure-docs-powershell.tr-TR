---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106381"
---
# <span data-ttu-id="a2339-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a2339-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="a2339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2339-102">SYNOPSIS</span></span>
<span data-ttu-id="a2339-103">Bir Azure RemoteApp koleksiyonuna Kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="a2339-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a2339-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2339-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2339-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2339-105">DESCRIPTION</span></span>
<span data-ttu-id="a2339-106">**Add-AzureRemoteAppUser** cmdlet 'ı bir Azure RemoteApp koleksiyonuna Kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="a2339-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a2339-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2339-107">EXAMPLES</span></span>

### <span data-ttu-id="a2339-108">Örnek 1: Microsoft hesabı kullanarak Kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="a2339-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="a2339-109">Bu komut Microsoft hesabını PattiFuller@contoso.com contoso adlı koleksiyona ekler.</span><span class="sxs-lookup"><span data-stu-id="a2339-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="a2339-110">Örnek 2: Azure Active Directory hesabını kullanarak Kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="a2339-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="a2339-111">Bu komut Azure Active Directory hesabını PattiFuller@contoso.com contoso adlı koleksiyona ekler.</span><span class="sxs-lookup"><span data-stu-id="a2339-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="a2339-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2339-112">PARAMETERS</span></span>

### <span data-ttu-id="a2339-113">-Diğer ad</span><span class="sxs-lookup"><span data-stu-id="a2339-113">-Alias</span></span>
<span data-ttu-id="a2339-114">Yayımlanmış bir program diğer adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2339-114">Specifies a published program alias.</span></span>
<span data-ttu-id="a2339-115">Bu parametreyi yalnızca uygulama başına yayımlama modunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2339-115">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2339-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a2339-116">-CollectionName</span></span>
<span data-ttu-id="a2339-117">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2339-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2339-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2339-118">-Profile</span></span>
<span data-ttu-id="a2339-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2339-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2339-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a2339-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2339-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="a2339-121">-Type</span></span>
<span data-ttu-id="a2339-122">Kullanıcı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2339-122">Specifies a user type.</span></span>
<span data-ttu-id="a2339-123">Bu parametre için kabul edilebilir değerler: OrgID veya MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="a2339-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2339-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="a2339-124">-UserUpn</span></span>
<span data-ttu-id="a2339-125">Kullanıcının Kullanıcı asıl adını (UPN) belirtir; Örneğin PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="a2339-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2339-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2339-126">CommonParameters</span></span>
<span data-ttu-id="a2339-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2339-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2339-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2339-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2339-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2339-129">INPUTS</span></span>

## <span data-ttu-id="a2339-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2339-130">OUTPUTS</span></span>

## <span data-ttu-id="a2339-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2339-131">NOTES</span></span>

## <span data-ttu-id="a2339-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2339-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2339-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a2339-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="a2339-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="a2339-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


