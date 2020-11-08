---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105703"
---
# <span data-ttu-id="87f41-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="87f41-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="87f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f41-102">SYNOPSIS</span></span>
<span data-ttu-id="87f41-103">Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87f41-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="87f41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87f41-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87f41-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87f41-105">DESCRIPTION</span></span>
<span data-ttu-id="87f41-106">**Clear-Azureremoteappvmetradobject** cmdlet 'ı, Azure Active Directory 'de artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87f41-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="87f41-107">Azure Active Directory nesnelerini kaldırma hakkına sahip kimlik bilgilerini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="87f41-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="87f41-108">*Ayrıntılı* ortak parametreyi belirtirseniz, bu cmdlet sildiği her nesnenin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="87f41-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="87f41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87f41-109">EXAMPLES</span></span>

### <span data-ttu-id="87f41-110">Örnek 1: koleksiyon için eski nesneleri Temizleme</span><span class="sxs-lookup"><span data-stu-id="87f41-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="87f41-111">İlk komut, **Get-Credential** kullanarak bir Kullanıcı adı ve parola ister.</span><span class="sxs-lookup"><span data-stu-id="87f41-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="87f41-112">Komut sonuçları $AdminCredentials değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="87f41-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="87f41-113">İkinci komut contoso adlı koleksiyon için eski nesneleri temizler.</span><span class="sxs-lookup"><span data-stu-id="87f41-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="87f41-114">Komut $AdminCredentials değişkeninde depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="87f41-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="87f41-115">Komutun başarılı olabilmesi için, bu kimlik bilgilerinin uygun haklara sahip olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="87f41-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="87f41-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87f41-116">PARAMETERS</span></span>

### <span data-ttu-id="87f41-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="87f41-117">-CollectionName</span></span>
<span data-ttu-id="87f41-118">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f41-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f41-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="87f41-119">-Credential</span></span>
<span data-ttu-id="87f41-120">Bu eylemi gerçekleştirme hakkına sahip bir kimlik bilgisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f41-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="87f41-121">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="87f41-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="87f41-122">Bu parametreyi belirtmezseniz, bu cmdlet geçerli kullanıcı kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="87f41-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f41-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="87f41-123">-Profile</span></span>
<span data-ttu-id="87f41-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87f41-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87f41-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="87f41-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87f41-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="87f41-126">-Confirm</span></span>
<span data-ttu-id="87f41-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87f41-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f41-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f41-128">-WhatIf</span></span>
<span data-ttu-id="87f41-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87f41-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f41-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87f41-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f41-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f41-131">CommonParameters</span></span>
<span data-ttu-id="87f41-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87f41-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f41-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f41-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f41-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87f41-134">INPUTS</span></span>

## <span data-ttu-id="87f41-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87f41-135">OUTPUTS</span></span>

## <span data-ttu-id="87f41-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87f41-136">NOTES</span></span>

## <span data-ttu-id="87f41-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87f41-137">RELATED LINKS</span></span>

[<span data-ttu-id="87f41-138">Get-Azureremoteappvmeleadobject</span><span class="sxs-lookup"><span data-stu-id="87f41-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


