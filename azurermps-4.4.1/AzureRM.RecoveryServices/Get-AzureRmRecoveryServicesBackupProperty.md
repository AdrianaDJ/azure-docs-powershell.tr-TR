---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763642"
---
# <span data-ttu-id="483aa-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="483aa-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="483aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483aa-102">SYNOPSIS</span></span>
<span data-ttu-id="483aa-103">Yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="483aa-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="483aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="483aa-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="483aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="483aa-105">DESCRIPTION</span></span>
<span data-ttu-id="483aa-106">**Get-AzureRmRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="483aa-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="483aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="483aa-107">EXAMPLES</span></span>

## <span data-ttu-id="483aa-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="483aa-108">PARAMETERS</span></span>

### <span data-ttu-id="483aa-109">-Kasa</span><span class="sxs-lookup"><span data-stu-id="483aa-109">-Vault</span></span>
<span data-ttu-id="483aa-110">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="483aa-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="483aa-111">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="483aa-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="483aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483aa-112">-DefaultProfile</span></span>
<span data-ttu-id="483aa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="483aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="483aa-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483aa-114">CommonParameters</span></span>
<span data-ttu-id="483aa-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="483aa-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483aa-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483aa-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483aa-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="483aa-117">INPUTS</span></span>

### <span data-ttu-id="483aa-118">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="483aa-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="483aa-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="483aa-119">OUTPUTS</span></span>

### <span data-ttu-id="483aa-120">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="483aa-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="483aa-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="483aa-121">NOTES</span></span>

## <span data-ttu-id="483aa-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="483aa-122">RELATED LINKS</span></span>

