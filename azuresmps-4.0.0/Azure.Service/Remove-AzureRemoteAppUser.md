---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105866"
---
# <span data-ttu-id="dd2ae-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dd2ae-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="dd2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2ae-103">Bir Azure RemoteApp koleksiyonundan kullanıcı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dd2ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd2ae-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd2ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd2ae-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2ae-106">**Remove-AzureRemoteAppUser** cmdlet 'i, bir kullanıcıyı Azure RemoteApp koleksiyonundan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dd2ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd2ae-107">EXAMPLES</span></span>

### <span data-ttu-id="dd2ae-108">Example1: koleksiyondan Kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="dd2ae-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="dd2ae-109">Bu komut, contoso koleksiyonundan Azure ActiveDirectory kullanıcısını kaldırır PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dd2ae-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="dd2ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd2ae-110">PARAMETERS</span></span>

### <span data-ttu-id="dd2ae-111">-Diğer ad</span><span class="sxs-lookup"><span data-stu-id="dd2ae-111">-Alias</span></span>
<span data-ttu-id="dd2ae-112">Yayımlanmış bir program diğer adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-112">Specifies a published program alias.</span></span>
<span data-ttu-id="dd2ae-113">Bu parametreyi yalnızca uygulama başına yayımlama modunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="dd2ae-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="dd2ae-114">-CollectionName</span></span>
<span data-ttu-id="dd2ae-115">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="dd2ae-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="dd2ae-116">-Profile</span></span>
<span data-ttu-id="dd2ae-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd2ae-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd2ae-119">-Tür</span><span class="sxs-lookup"><span data-stu-id="dd2ae-119">-Type</span></span>
<span data-ttu-id="dd2ae-120">Kullanıcı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-120">Specifies a user type.</span></span>
<span data-ttu-id="dd2ae-121">Bu parametre için kabul edilebilir değerler: OrgID veya MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="dd2ae-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="dd2ae-122">-UserUpn</span></span>
<span data-ttu-id="dd2ae-123">Kullanıcının Kullanıcı asıl adını (UPN) belirtir; Örneğin user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dd2ae-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="dd2ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2ae-124">CommonParameters</span></span>
<span data-ttu-id="dd2ae-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd2ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2ae-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2ae-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd2ae-127">INPUTS</span></span>

## <span data-ttu-id="dd2ae-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd2ae-128">OUTPUTS</span></span>

## <span data-ttu-id="dd2ae-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd2ae-129">NOTES</span></span>

## <span data-ttu-id="dd2ae-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd2ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd2ae-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dd2ae-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="dd2ae-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dd2ae-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


