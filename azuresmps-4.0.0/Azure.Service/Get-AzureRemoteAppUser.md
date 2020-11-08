---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106316"
---
# <span data-ttu-id="270a8-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="270a8-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="270a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270a8-102">SYNOPSIS</span></span>
<span data-ttu-id="270a8-103">Azure RemoteApp koleksiyonundaki kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="270a8-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="270a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="270a8-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="270a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="270a8-105">DESCRIPTION</span></span>
<span data-ttu-id="270a8-106">**Get-AzureRemoteAppUser** cmdlet 'ı bir Azure RemoteApp koleksiyonundaki kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="270a8-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="270a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="270a8-107">EXAMPLES</span></span>

### <span data-ttu-id="270a8-108">Örnek 1: bir koleksiyonun kullanıcılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="270a8-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="270a8-109">Bu komut, contoso adlı Azure RemoteApp koleksiyonuna erişimi olan kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="270a8-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="270a8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="270a8-110">PARAMETERS</span></span>

### <span data-ttu-id="270a8-111">-Diğer ad</span><span class="sxs-lookup"><span data-stu-id="270a8-111">-Alias</span></span>
<span data-ttu-id="270a8-112">Yayımlanmış bir program diğer adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="270a8-112">Specifies a published program alias.</span></span>
<span data-ttu-id="270a8-113">Bu parametreyi yalnızca uygulama başına yayımlama modunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="270a8-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="270a8-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="270a8-114">-CollectionName</span></span>
<span data-ttu-id="270a8-115">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="270a8-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="270a8-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="270a8-116">-Profile</span></span>
<span data-ttu-id="270a8-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="270a8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="270a8-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="270a8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="270a8-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="270a8-119">-UserUpn</span></span>
<span data-ttu-id="270a8-120">Bilgileri listelemek üzere bir kullanıcının Kullanıcı asıl adını (UPN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="270a8-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="270a8-121">Örneğin, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="270a8-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="270a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270a8-122">CommonParameters</span></span>
<span data-ttu-id="270a8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="270a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270a8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270a8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="270a8-125">INPUTS</span></span>

## <span data-ttu-id="270a8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="270a8-126">OUTPUTS</span></span>

## <span data-ttu-id="270a8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="270a8-127">NOTES</span></span>

## <span data-ttu-id="270a8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="270a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="270a8-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="270a8-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="270a8-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="270a8-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="270a8-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="270a8-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


