---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106147"
---
# <span data-ttu-id="81ebd-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="81ebd-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="81ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="81ebd-103">Bir Azure RemoteApp koleksiyonundan kullanıcının Kullanıcı diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81ebd-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="81ebd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81ebd-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81ebd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="81ebd-106">**Remove-Azureremoteappuserdısk** cmdlet 'ı bir Azure RemoteApp koleksiyonundan bir kullanıcının Kullanıcı diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81ebd-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="81ebd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81ebd-107">EXAMPLES</span></span>

### <span data-ttu-id="81ebd-108">Örnek 1: Kullanıcı diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="81ebd-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="81ebd-109">Bu komut, Contoso01 Collection 'ı içeren bir Azure Active Directory kullanıcısının Kullanıcı diskini kaldırır PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="81ebd-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="81ebd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81ebd-110">PARAMETERS</span></span>

### <span data-ttu-id="81ebd-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="81ebd-111">-CollectionName</span></span>
<span data-ttu-id="81ebd-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81ebd-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="81ebd-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="81ebd-113">-Profile</span></span>
<span data-ttu-id="81ebd-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81ebd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81ebd-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="81ebd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81ebd-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="81ebd-116">-UserUpn</span></span>
<span data-ttu-id="81ebd-117">Bu cmdlet 'in diski kaldırdığı kullanıcının Kullanıcı asıl adını (UPN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="81ebd-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="81ebd-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="81ebd-118">-Confirm</span></span>
<span data-ttu-id="81ebd-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81ebd-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ebd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ebd-120">-WhatIf</span></span>
<span data-ttu-id="81ebd-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81ebd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81ebd-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81ebd-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ebd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ebd-123">CommonParameters</span></span>
<span data-ttu-id="81ebd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81ebd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ebd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ebd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ebd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81ebd-126">INPUTS</span></span>

## <span data-ttu-id="81ebd-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81ebd-127">OUTPUTS</span></span>

## <span data-ttu-id="81ebd-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81ebd-128">NOTES</span></span>

## <span data-ttu-id="81ebd-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81ebd-129">RELATED LINKS</span></span>

[<span data-ttu-id="81ebd-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="81ebd-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


