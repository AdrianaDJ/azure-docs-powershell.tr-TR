---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105698"
---
# <span data-ttu-id="e3de8-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="e3de8-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="e3de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3de8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3de8-103">Bir kullanıcının Kullanıcı diskini bir Azure RemoteApp koleksiyonundan diğerine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="e3de8-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="e3de8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3de8-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3de8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3de8-105">DESCRIPTION</span></span>
<span data-ttu-id="e3de8-106">**Copy-AzureRemoteAppUserDisk** cmdlet 'ı bir Azure RemoteApp koleksiyonundan bir kullanıcının Kullanıcı diskini bir başkasına kopyalar.</span><span class="sxs-lookup"><span data-stu-id="e3de8-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="e3de8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3de8-107">EXAMPLES</span></span>

### <span data-ttu-id="e3de8-108">Örnek 1: Kullanıcı diski kopyalama</span><span class="sxs-lookup"><span data-stu-id="e3de8-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="e3de8-109">Bu komut, UPN Contoso01 olan bir Azure Active Directory kullanıcısının Kullanıcı diskini koleksiyon PattiFuller@contoso.com Contoso02 'e kopyalar.</span><span class="sxs-lookup"><span data-stu-id="e3de8-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="e3de8-110">PattiFuller@contoso.comContoso02 'da zaten bir Kullanıcı diski varsa, bu komut bunu geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="e3de8-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="e3de8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3de8-111">PARAMETERS</span></span>

### <span data-ttu-id="e3de8-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="e3de8-112">-DestinationCollectionName</span></span>
<span data-ttu-id="e3de8-113">Hedef Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3de8-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de8-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="e3de8-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="e3de8-115">Bu cmdlet 'in var olan bir Kullanıcı diskinin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3de8-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3de8-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3de8-116">-Profile</span></span>
<span data-ttu-id="e3de8-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3de8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3de8-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e3de8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3de8-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e3de8-119">-SourceCollectionName</span></span>
<span data-ttu-id="e3de8-120">Kaynak Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3de8-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de8-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e3de8-121">-UserUpn</span></span>
<span data-ttu-id="e3de8-122">Bu cmdlet 'in diski kopyaladığı kullanıcının Kullanıcı asıl adını (UPN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3de8-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3de8-123">CommonParameters</span></span>
<span data-ttu-id="e3de8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3de8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3de8-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3de8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3de8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3de8-126">INPUTS</span></span>

## <span data-ttu-id="e3de8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3de8-127">OUTPUTS</span></span>

## <span data-ttu-id="e3de8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3de8-128">NOTES</span></span>

## <span data-ttu-id="e3de8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3de8-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3de8-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="e3de8-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


