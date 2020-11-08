---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105593"
---
# <span data-ttu-id="89185-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="89185-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="89185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89185-102">SYNOPSIS</span></span>
<span data-ttu-id="89185-103">Site kurtarma Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="89185-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="89185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89185-104">SYNTAX</span></span>

### <span data-ttu-id="89185-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89185-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="89185-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="89185-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="89185-107">ByName</span><span class="sxs-lookup"><span data-stu-id="89185-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89185-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="89185-108">DESCRIPTION</span></span>
<span data-ttu-id="89185-109">**Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ı geçerli Azure Site Recovery Kasası için koruma kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="89185-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="89185-110">Koruma kapsayıcısı sanal makineler gibi korumalı nesneler için mantıksal bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="89185-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="89185-111">Koruma ilkeleri, korumalı öğeler için çoğaltma ayarlarını tanımlar ve bir koruma konteyneriyle ilişkilendirilebilir ve korumalı bir varlığa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="89185-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="89185-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89185-112">EXAMPLES</span></span>

### <span data-ttu-id="89185-113">Örnek 1: korumalı kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="89185-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="89185-114">Bu komut, geçerli kasa için korumalı kapsayıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="89185-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="89185-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89185-115">PARAMETERS</span></span>

### <span data-ttu-id="89185-116">-ID</span><span class="sxs-lookup"><span data-stu-id="89185-116">-Id</span></span>
<span data-ttu-id="89185-117">Bir korumalı kapsayıcının alınacağı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89185-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89185-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="89185-118">-Name</span></span>
<span data-ttu-id="89185-119">Alınacak bir koruma kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89185-119">Specifies the name of a protection container to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89185-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="89185-120">-Profile</span></span>
<span data-ttu-id="89185-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89185-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89185-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="89185-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89185-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89185-123">CommonParameters</span></span>
<span data-ttu-id="89185-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89185-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89185-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89185-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89185-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89185-126">INPUTS</span></span>

## <span data-ttu-id="89185-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89185-127">OUTPUTS</span></span>

## <span data-ttu-id="89185-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89185-128">NOTES</span></span>

## <span data-ttu-id="89185-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89185-129">RELATED LINKS</span></span>

[<span data-ttu-id="89185-130">Azure Site Recovery Hizmetleri cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="89185-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


