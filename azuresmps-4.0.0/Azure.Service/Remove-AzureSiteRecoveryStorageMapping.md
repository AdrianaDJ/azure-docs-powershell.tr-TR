---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106109"
---
# <span data-ttu-id="3ffd5-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="3ffd5-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="3ffd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ffd5-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffd5-103">Site kurtarma Kasası için depolama nesnesi eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="3ffd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ffd5-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ffd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ffd5-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffd5-106">**Remove-AzureSiteRecoveryStorageMapping** cmdlet 'i, geçerli Azure Site Recovery Kasası Için bir depolama nesnesi eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="3ffd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ffd5-107">EXAMPLES</span></span>

### <span data-ttu-id="3ffd5-108">Örnek 1: ağ ile kurtarma ağı arasındaki eşlemeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="3ffd5-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="3ffd5-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="3ffd5-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="3ffd5-111">İkinci komut iki depolama nesnesi arasındaki eşlemeyi alır ve $StorageMapping değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="3ffd5-112">Komut, $Servers ilk öğesi olarak ağ eşlemesinin birincil sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="3ffd5-113">Komut, kurtarma ağının sunucusunu $Servers ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="3ffd5-114">Son komut $StorageMapping olan eşlemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="3ffd5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ffd5-115">PARAMETERS</span></span>

### <span data-ttu-id="3ffd5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ffd5-116">-Profile</span></span>
<span data-ttu-id="3ffd5-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ffd5-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ffd5-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="3ffd5-119">-StorageMapping</span></span>
<span data-ttu-id="3ffd5-120">Ağ eşlemesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-120">Specifies a network mapping.</span></span>
<span data-ttu-id="3ffd5-121">Bir **Asrstoragemapping** edinmek için **Get-AzureSiteRecoveryStorage** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffd5-122">CommonParameters</span></span>
<span data-ttu-id="3ffd5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ffd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffd5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffd5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ffd5-125">INPUTS</span></span>

## <span data-ttu-id="3ffd5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ffd5-126">OUTPUTS</span></span>

## <span data-ttu-id="3ffd5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ffd5-127">NOTES</span></span>

## <span data-ttu-id="3ffd5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ffd5-128">RELATED LINKS</span></span>

[<span data-ttu-id="3ffd5-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="3ffd5-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


