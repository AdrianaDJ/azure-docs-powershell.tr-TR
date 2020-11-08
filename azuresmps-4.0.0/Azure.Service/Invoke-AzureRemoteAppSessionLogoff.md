---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106247"
---
# <span data-ttu-id="1f349-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="1f349-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="1f349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f349-102">SYNOPSIS</span></span>
<span data-ttu-id="1f349-103">Azure RemoteApp oturumunun hemen oturumunu kapatır.</span><span class="sxs-lookup"><span data-stu-id="1f349-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="1f349-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f349-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f349-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f349-105">DESCRIPTION</span></span>
<span data-ttu-id="1f349-106">**Invoke-AzureRemoteAppSessionLogoff** cmdlet 'i, bir kullanıcıyı Azure RemoteApp 'te çalışan bir uzak oturumdan hemen kapatır.</span><span class="sxs-lookup"><span data-stu-id="1f349-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="1f349-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f349-107">EXAMPLES</span></span>

### <span data-ttu-id="1f349-108">Örnek 1: kullanıcının oturumunu kapatma</span><span class="sxs-lookup"><span data-stu-id="1f349-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="1f349-109">Bu komut, UPN 'si olan kullanıcıyı kapatır PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1f349-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="1f349-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f349-110">PARAMETERS</span></span>

### <span data-ttu-id="1f349-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1f349-111">-CollectionName</span></span>
<span data-ttu-id="1f349-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f349-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1f349-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="1f349-113">-Profile</span></span>
<span data-ttu-id="1f349-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f349-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f349-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1f349-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f349-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="1f349-116">-UserUpn</span></span>
<span data-ttu-id="1f349-117">Bir kullanıcının Kullanıcı asıl adını (UPN), örneğin PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1f349-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f349-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f349-118">-Confirm</span></span>
<span data-ttu-id="1f349-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f349-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f349-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f349-120">-WhatIf</span></span>
<span data-ttu-id="1f349-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f349-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f349-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f349-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f349-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f349-123">CommonParameters</span></span>
<span data-ttu-id="1f349-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f349-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f349-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f349-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f349-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f349-126">INPUTS</span></span>

## <span data-ttu-id="1f349-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f349-127">OUTPUTS</span></span>

## <span data-ttu-id="1f349-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f349-128">NOTES</span></span>

## <span data-ttu-id="1f349-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f349-129">RELATED LINKS</span></span>

[<span data-ttu-id="1f349-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1f349-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="1f349-131">Bağlantısı kesiliyor-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1f349-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="1f349-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1f349-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


