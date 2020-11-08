---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105563"
---
# <span data-ttu-id="b1690-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b1690-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="b1690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1690-102">SYNOPSIS</span></span>
<span data-ttu-id="b1690-103">Cihazda birim kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b1690-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="b1690-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1690-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1690-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1690-105">DESCRIPTION</span></span>
<span data-ttu-id="b1690-106">**Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'i, bir aygıttaki birim kapsayıcılarının veya belirtilen ada sahip birim kapsayıcısının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b1690-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="b1690-107">Döndürülen nesne aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="b1690-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="b1690-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="b1690-108">**BandwidthRate**</span></span>
- <span data-ttu-id="b1690-109">**Şifrelemetuşu**</span><span class="sxs-lookup"><span data-stu-id="b1690-109">**EncryptionKey**</span></span>
- <span data-ttu-id="b1690-110">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="b1690-110">**InstanceId**</span></span>
- <span data-ttu-id="b1690-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="b1690-111">**IsDefault**</span></span>
- <span data-ttu-id="b1690-112">**Isencryptionenabled**</span><span class="sxs-lookup"><span data-stu-id="b1690-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="b1690-113">**Adlandır**</span><span class="sxs-lookup"><span data-stu-id="b1690-113">**Name**</span></span>
- <span data-ttu-id="b1690-114">**Operationınprogress**</span><span class="sxs-lookup"><span data-stu-id="b1690-114">**OperationInProgress**</span></span>
- <span data-ttu-id="b1690-115">**Aitse**</span><span class="sxs-lookup"><span data-stu-id="b1690-115">**Owned**</span></span>
- <span data-ttu-id="b1690-116">**Primarystoragecredential**</span><span class="sxs-lookup"><span data-stu-id="b1690-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="b1690-117">**Secretsencryptionparmak Izi**</span><span class="sxs-lookup"><span data-stu-id="b1690-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="b1690-118">**Birimsayısı**</span><span class="sxs-lookup"><span data-stu-id="b1690-118">**VolumeCount**</span></span>

## <span data-ttu-id="b1690-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1690-119">EXAMPLES</span></span>

### <span data-ttu-id="b1690-120">Örnek 1: cihazdaki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="b1690-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="b1690-121">Bu komut, 8600-Bravo 001 adlı aygıttaki birim kapsayıcılarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b1690-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="b1690-122">Örnek 2: adını kullanarak kapsayıcı alma</span><span class="sxs-lookup"><span data-stu-id="b1690-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="b1690-123">Bu komut, Contoso63-AppVm adındaki cihazda Container08 adlı birim kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="b1690-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="b1690-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1690-124">PARAMETERS</span></span>

### <span data-ttu-id="b1690-125">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="b1690-125">-DeviceName</span></span>
<span data-ttu-id="b1690-126">StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1690-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="b1690-127">Bu cmdlet, bu parametrenin belirttiği cihazdan birim kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b1690-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1690-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1690-128">-Profile</span></span>
<span data-ttu-id="b1690-129">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1690-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1690-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="b1690-130">-VolumeContainerName</span></span>
<span data-ttu-id="b1690-131">Alınacak birim kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1690-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1690-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1690-132">CommonParameters</span></span>
<span data-ttu-id="b1690-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1690-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1690-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1690-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1690-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1690-135">INPUTS</span></span>

### <span data-ttu-id="b1690-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1690-136">None</span></span>

## <span data-ttu-id="b1690-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1690-137">OUTPUTS</span></span>

### <span data-ttu-id="b1690-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="b1690-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="b1690-139">Bu cmdlet, *Volumecontainername* parametresini belirttiğinizde bir **datacontainer** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1690-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="b1690-140">Bu parametreyi belirtmezseniz, bu cmdlet bir **IList \<DataContainer\>** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1690-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="b1690-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1690-141">NOTES</span></span>

## <span data-ttu-id="b1690-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1690-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1690-143">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b1690-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="b1690-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b1690-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


