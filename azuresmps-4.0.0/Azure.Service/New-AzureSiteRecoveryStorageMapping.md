---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105975"
---
# <span data-ttu-id="fc047-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="fc047-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="fc047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc047-102">SYNOPSIS</span></span>
<span data-ttu-id="fc047-103">Azure depolama nesnesi ile kurtarma depolama nesnesi arasında eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc047-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="fc047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc047-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fc047-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc047-105">DESCRIPTION</span></span>
<span data-ttu-id="fc047-106">**New-AzureSiteRecoveryStorageMapping** cmdlet 'ı Azure Site Recovery yönetilen birincil Azure depolama nesnesi Ile kurtarma depolama nesnesi arasında eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc047-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="fc047-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc047-107">EXAMPLES</span></span>

### <span data-ttu-id="fc047-108">Örnek 1: depolama nesnesiyle kurtarma depolama nesnesi arasında eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc047-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="fc047-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="fc047-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="fc047-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="fc047-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="fc047-111">İkinci komut $Servers dizisindeki ilk sunucunun site kurtarma depolamasını alır ve $Storages depolar.</span><span class="sxs-lookup"><span data-stu-id="fc047-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="fc047-112">Son komutu birincil ağla kurtarma ağı arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc047-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="fc047-113">Komut birincil depolama nesnesini $Storages ilk öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc047-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="fc047-114">Komut, kurtarma depolama nesnesini $Storages ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc047-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="fc047-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc047-115">PARAMETERS</span></span>

### <span data-ttu-id="fc047-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="fc047-116">-PrimaryStorage</span></span>
<span data-ttu-id="fc047-117">Kurtarma depolama alanı ile eşlenecek birincil depolamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc047-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="fc047-118">Bir **Asrstorage** nesnesi almak için Get-AzureSiteRecoveryStorage cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc047-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc047-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc047-119">-Profile</span></span>
<span data-ttu-id="fc047-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc047-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc047-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fc047-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc047-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="fc047-122">-RecoveryStorage</span></span>
<span data-ttu-id="fc047-123">Kurtarma depolama nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc047-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="fc047-124">Bu cmdlet birincil depolama nesnesini bu parametrenin belirttiği depolama nesnesiyle eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc047-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="fc047-125">Bir **Asrstorage** nesnesi almak için **Get-AzureSiteRecoveryStorage** kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc047-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc047-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc047-126">CommonParameters</span></span>
<span data-ttu-id="fc047-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc047-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc047-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc047-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc047-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc047-129">INPUTS</span></span>

## <span data-ttu-id="fc047-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc047-130">OUTPUTS</span></span>

## <span data-ttu-id="fc047-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc047-131">NOTES</span></span>

## <span data-ttu-id="fc047-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc047-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc047-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="fc047-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="fc047-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="fc047-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="fc047-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="fc047-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


