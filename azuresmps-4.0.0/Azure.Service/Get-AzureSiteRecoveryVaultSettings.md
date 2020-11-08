---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106566"
---
# <span data-ttu-id="8ef71-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8ef71-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="8ef71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef71-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef71-103">Site kurtarma Kasası ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8ef71-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="8ef71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ef71-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8ef71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ef71-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef71-106">**Get-AzureSiteRecoveryVaultSettings** cmdlet 'ı geçerli Azure Site Recovery kasası ile ilgili ayarları alır.</span><span class="sxs-lookup"><span data-stu-id="8ef71-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8ef71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ef71-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef71-108">Örnek 1: ayar bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="8ef71-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="8ef71-109">Bu komut, geçerli Azure Site Recovery Kasası için ayarlar bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="8ef71-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8ef71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ef71-110">PARAMETERS</span></span>

### <span data-ttu-id="8ef71-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="8ef71-111">-Profile</span></span>
<span data-ttu-id="8ef71-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ef71-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ef71-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8ef71-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ef71-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef71-114">CommonParameters</span></span>
<span data-ttu-id="8ef71-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ef71-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef71-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef71-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef71-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ef71-117">INPUTS</span></span>

## <span data-ttu-id="8ef71-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ef71-118">OUTPUTS</span></span>

## <span data-ttu-id="8ef71-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ef71-119">NOTES</span></span>

## <span data-ttu-id="8ef71-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ef71-120">RELATED LINKS</span></span>

[<span data-ttu-id="8ef71-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8ef71-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="8ef71-122">İçeri aktarma-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8ef71-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


