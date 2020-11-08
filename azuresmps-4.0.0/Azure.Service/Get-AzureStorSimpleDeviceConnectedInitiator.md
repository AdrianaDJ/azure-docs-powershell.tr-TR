---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106291"
---
# <span data-ttu-id="76e3a-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="76e3a-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="76e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="76e3a-103">StorSimple aygıtı için sağlanan Iscsı bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="76e3a-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="76e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76e3a-104">SYNTAX</span></span>

### <span data-ttu-id="76e3a-105">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="76e3a-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="76e3a-106">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="76e3a-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="76e3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="76e3a-108">**Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet 'ı StorSimple aygıtı Için sağlanan iSCSI bağlantılarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="76e3a-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="76e3a-109">Bu cmdlet 'in döndürdüğü Iscsı bağlantı nesneleri aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="76e3a-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="76e3a-110">**Acrınstanceıd**</span><span class="sxs-lookup"><span data-stu-id="76e3a-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="76e3a-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="76e3a-111">**AcrName**</span></span>
- <span data-ttu-id="76e3a-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="76e3a-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="76e3a-113">**Initiatoraddress**</span><span class="sxs-lookup"><span data-stu-id="76e3a-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="76e3a-114">**Arayüzler**</span><span class="sxs-lookup"><span data-stu-id="76e3a-114">**Interfaces**</span></span>
- <span data-ttu-id="76e3a-115">**'Si**</span><span class="sxs-lookup"><span data-stu-id="76e3a-115">**Iqn**</span></span>
- <span data-ttu-id="76e3a-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="76e3a-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="76e3a-117">Bu cmdlet yalnızca cihazda Iscsı bağlantıları açıksa bağlantı nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="76e3a-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="76e3a-118">Varsayılan olarak, bağlantılar kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="76e3a-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="76e3a-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76e3a-119">EXAMPLES</span></span>

### <span data-ttu-id="76e3a-120">Örnek 1: bir cihaz için tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="76e3a-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="76e3a-121">Bu komut, Contoso63-AppVm adlı aygıtın tüm Iscsı bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="76e3a-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="76e3a-122">Bu komut yalnızca cihazda bağlantılar açıksa bağlantı döndürür.</span><span class="sxs-lookup"><span data-stu-id="76e3a-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="76e3a-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76e3a-123">PARAMETERS</span></span>

### <span data-ttu-id="76e3a-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="76e3a-124">-DeviceId</span></span>
<span data-ttu-id="76e3a-125">Iscsı başlatıcılarının alınacağı StorSimple aygıtının örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76e3a-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e3a-126">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="76e3a-126">-DeviceName</span></span>
<span data-ttu-id="76e3a-127">Iscsı başlatıcılarının alınacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76e3a-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e3a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="76e3a-128">-Profile</span></span>
<span data-ttu-id="76e3a-129">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="76e3a-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="76e3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e3a-130">CommonParameters</span></span>
<span data-ttu-id="76e3a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76e3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e3a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e3a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e3a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76e3a-133">INPUTS</span></span>

### <span data-ttu-id="76e3a-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76e3a-134">None</span></span>

## <span data-ttu-id="76e3a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76e3a-135">OUTPUTS</span></span>

### <span data-ttu-id="76e3a-136">Listeniz\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="76e3a-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="76e3a-137">Bu cmdlet, aşağıdaki özellikleri içeren bir Iscsı bağlantı nesnesi döndürür:</span><span class="sxs-lookup"><span data-stu-id="76e3a-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="76e3a-138">**Acrınstanceıd**</span><span class="sxs-lookup"><span data-stu-id="76e3a-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="76e3a-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="76e3a-139">**AcrName**</span></span>
- <span data-ttu-id="76e3a-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="76e3a-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="76e3a-141">**Initiatoraddress**</span><span class="sxs-lookup"><span data-stu-id="76e3a-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="76e3a-142">**Arayüzler**</span><span class="sxs-lookup"><span data-stu-id="76e3a-142">**Interfaces**</span></span>
- <span data-ttu-id="76e3a-143">**'Si**</span><span class="sxs-lookup"><span data-stu-id="76e3a-143">**Iqn**</span></span>
- <span data-ttu-id="76e3a-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="76e3a-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="76e3a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76e3a-145">NOTES</span></span>

## <span data-ttu-id="76e3a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76e3a-146">RELATED LINKS</span></span>

[<span data-ttu-id="76e3a-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="76e3a-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


