---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105678"
---
# <span data-ttu-id="40d9b-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="40d9b-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="40d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="40d9b-103">Tüm Kullanıcı disklerini bir Azure RemoteApp koleksiyonundan belirtilen Azure depolama hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="40d9b-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="40d9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40d9b-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d9b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="40d9b-106">**Export-AzureRemoteAppUserDisk** cmdlet 'i, tüm Kullanıcı disklerini bir Azure RemoteApp koleksiyonundan belirtilen Azure depolama hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="40d9b-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="40d9b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40d9b-107">EXAMPLES</span></span>

### <span data-ttu-id="40d9b-108">Örnek 1: koleksiyondan tüm Kullanıcı disklerini belirtilen Azure depolama hesabına dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="40d9b-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="40d9b-109">Bu komut, contoso adlı koleksiyondaki tüm Kullanıcı disklerini, ad AccountName ve anahtar AccountKey ile belirtilen Azure depolama hesabındaki ContainerName adlı kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="40d9b-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="40d9b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40d9b-110">PARAMETERS</span></span>

### <span data-ttu-id="40d9b-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="40d9b-111">-CollectionName</span></span>
<span data-ttu-id="40d9b-112">Kaynak Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="40d9b-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="40d9b-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="40d9b-114">Hedef Azure depolama hesabında bir kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d9b-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="40d9b-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="40d9b-116">Hedef Azure depolama hesabının anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-116">Specifies the Key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="40d9b-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40d9b-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="40d9b-118">Hedef Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="40d9b-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="40d9b-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="40d9b-120">Cmdlet 'in var olan Kullanıcı diskinin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="40d9b-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="40d9b-121">-Profile</span></span>
<span data-ttu-id="40d9b-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40d9b-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="40d9b-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40d9b-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="40d9b-124">-Confirm</span></span>
<span data-ttu-id="40d9b-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40d9b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d9b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d9b-126">-WhatIf</span></span>
<span data-ttu-id="40d9b-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40d9b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d9b-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40d9b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d9b-129">CommonParameters</span></span>
<span data-ttu-id="40d9b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40d9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d9b-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d9b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d9b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40d9b-132">INPUTS</span></span>

## <span data-ttu-id="40d9b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40d9b-133">OUTPUTS</span></span>

## <span data-ttu-id="40d9b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40d9b-134">NOTES</span></span>

## <span data-ttu-id="40d9b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40d9b-135">RELATED LINKS</span></span>

[<span data-ttu-id="40d9b-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="40d9b-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="40d9b-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="40d9b-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


