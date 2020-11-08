---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106260"
---
# <span data-ttu-id="1f4a7-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1f4a7-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="1f4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4a7-103">Site Recovery kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="1f4a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f4a7-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f4a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f4a7-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4a7-106">**Import-AzureSiteRecoveryVaultSettingsFile** cmdlet 'i, geçerli oturumdaki sonraki site kurtarma işlemleri için kasa bağlamını ayarlamak üzere bir Azure Site Recovery kasa ayarları dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="1f4a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f4a7-107">EXAMPLES</span></span>

### <span data-ttu-id="1f4a7-108">Örnek 1: kasa ayarları dosyasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="1f4a7-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="1f4a7-109">Bu komut, belirtilen yoldaki kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="1f4a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f4a7-110">PARAMETERS</span></span>

### <span data-ttu-id="1f4a7-111">-Yol</span><span class="sxs-lookup"><span data-stu-id="1f4a7-111">-Path</span></span>
<span data-ttu-id="1f4a7-112">Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="1f4a7-113">Bu dosya, Site Recovery kasa portalından indirilebilir ve yerel olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4a7-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="1f4a7-114">-Profile</span></span>
<span data-ttu-id="1f4a7-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f4a7-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f4a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4a7-117">CommonParameters</span></span>
<span data-ttu-id="1f4a7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f4a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4a7-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4a7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f4a7-120">INPUTS</span></span>

## <span data-ttu-id="1f4a7-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f4a7-121">OUTPUTS</span></span>

## <span data-ttu-id="1f4a7-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f4a7-122">NOTES</span></span>

## <span data-ttu-id="1f4a7-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f4a7-123">RELATED LINKS</span></span>

[<span data-ttu-id="1f4a7-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1f4a7-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="1f4a7-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1f4a7-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


