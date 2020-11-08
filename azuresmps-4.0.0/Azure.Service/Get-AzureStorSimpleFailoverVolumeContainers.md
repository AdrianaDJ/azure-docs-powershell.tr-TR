---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105561"
---
# <span data-ttu-id="25658-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="25658-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="25658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25658-102">SYNOPSIS</span></span>
<span data-ttu-id="25658-103">Cihaz yük devretmesi için birim kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="25658-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="25658-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25658-104">SYNTAX</span></span>

### <span data-ttu-id="25658-105">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="25658-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25658-106">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="25658-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="25658-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="25658-107">DESCRIPTION</span></span>
<span data-ttu-id="25658-108">**Get-AzureStorSimpleFailoverVolumeContainers** cmdlet 'i cihaz yük devretmesi için birim kapsayıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="25658-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="25658-109">**Start-AzureStorSimpleDeviceFailover** cmdlet 'ine tek bir **birimkapsayıcısı** grubu veya **birimkapsayıcısı** gruplar dizisi geçirin.</span><span class="sxs-lookup"><span data-stu-id="25658-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="25658-110">Yalnızca **ısdcgroupeligıblefordr** özelliği için $true değeri olan gruplar yük devretmeye uygundur.</span><span class="sxs-lookup"><span data-stu-id="25658-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="25658-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25658-111">EXAMPLES</span></span>

### <span data-ttu-id="25658-112">Örnek 1: yük devretme birimi kapsayıcılarını alma</span><span class="sxs-lookup"><span data-stu-id="25658-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="25658-113">Bu komut, yük devretme birimi kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="25658-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="25658-114">Yalnızca **ısdcgroupeligıblefordr** özelliği için $true değeri olan dcgroups cihaz yük devretmesi için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="25658-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="25658-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25658-115">PARAMETERS</span></span>

### <span data-ttu-id="25658-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="25658-116">-DeviceId</span></span>
<span data-ttu-id="25658-117">Cmdlet 'in çalıştırılacağı StorSimple aygıtının örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="25658-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25658-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="25658-118">-DeviceName</span></span>
<span data-ttu-id="25658-119">Cmdlet 'in çalıştırılacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25658-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25658-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="25658-120">-Profile</span></span>
<span data-ttu-id="25658-121">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="25658-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="25658-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25658-122">CommonParameters</span></span>
<span data-ttu-id="25658-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25658-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25658-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25658-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25658-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25658-125">INPUTS</span></span>

## <span data-ttu-id="25658-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25658-126">OUTPUTS</span></span>

### <span data-ttu-id="25658-127">'Te\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="25658-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="25658-128">Bu cmdlet, **Birimkapsayıcısı** gruplarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="25658-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="25658-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25658-129">NOTES</span></span>

## <span data-ttu-id="25658-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25658-130">RELATED LINKS</span></span>

[<span data-ttu-id="25658-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="25658-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="25658-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="25658-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


