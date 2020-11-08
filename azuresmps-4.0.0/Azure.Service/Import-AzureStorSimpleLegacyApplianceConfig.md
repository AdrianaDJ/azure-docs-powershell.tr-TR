---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106259"
---
# <span data-ttu-id="986ea-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="986ea-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="986ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986ea-102">SYNOPSIS</span></span>
<span data-ttu-id="986ea-103">Yapılandırma dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="986ea-103">Imports a configuration file.</span></span>

## <span data-ttu-id="986ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="986ea-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="986ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="986ea-105">DESCRIPTION</span></span>
<span data-ttu-id="986ea-106">**Import-AzureStorSimpleLegacyApplianceConfig** cmdlet 'i, eski olan gereç yapılandırma dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="986ea-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="986ea-107">Bu dosya, Azure StorSimple hizmeti için birim kapsayıcıları, yedekleme ilkeleri ve depolama hesabı kimlik bilgileri hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="986ea-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="986ea-108">Bu cmdlet, eski gereç yapılandırma meta verilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="986ea-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="986ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="986ea-109">EXAMPLES</span></span>

### <span data-ttu-id="986ea-110">Örnek 1: yapılandırma dosyasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="986ea-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="986ea-111">Bu komut, yapılandırma dosyasını belirtilen yolda içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="986ea-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="986ea-112">Komut dosyanın şifresini çözme anahtarını içerir.</span><span class="sxs-lookup"><span data-stu-id="986ea-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="986ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="986ea-113">PARAMETERS</span></span>

### <span data-ttu-id="986ea-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="986ea-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="986ea-115">Eski gereç yapılandırması için şifre çözme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="986ea-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="986ea-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="986ea-116">-ConfigFilePath</span></span>
<span data-ttu-id="986ea-117">Alınacak yapılandırma dosyasının mutlak yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="986ea-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="986ea-118">-Profile</span></span>
<span data-ttu-id="986ea-119">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="986ea-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="986ea-120">-Targetaygıtadı</span><span class="sxs-lookup"><span data-stu-id="986ea-120">-TargetDeviceName</span></span>
<span data-ttu-id="986ea-121">Portalda gösterilen hedef aygıtın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="986ea-121">Specifies the name of the target device as presented in the portal.</span></span>

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

### <span data-ttu-id="986ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986ea-122">CommonParameters</span></span>
<span data-ttu-id="986ea-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="986ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986ea-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986ea-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="986ea-125">INPUTS</span></span>

### <span data-ttu-id="986ea-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="986ea-126">None</span></span>

## <span data-ttu-id="986ea-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="986ea-127">OUTPUTS</span></span>

### <span data-ttu-id="986ea-128">Yasallık yapılandırma</span><span class="sxs-lookup"><span data-stu-id="986ea-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="986ea-129">Bu cmdlet, yapılandırmanın ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="986ea-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="986ea-130">**Yasallık Plianceconfiguration** nesnesi şu bilgileri içerir: yapılandırma kimliği, birim kapsayıcı adları, erişim denetim kayıtları, yedekleme ilkeleri, bant genişliği ayarları, birim kapsayıcıları, depolama hesabı kimlik bilgileri ve birimler.</span><span class="sxs-lookup"><span data-stu-id="986ea-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="986ea-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="986ea-131">NOTES</span></span>

## <span data-ttu-id="986ea-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="986ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="986ea-133">İçeri aktarma-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="986ea-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


