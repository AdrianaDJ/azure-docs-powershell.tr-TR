---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589392"
---
# <span data-ttu-id="9d182-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9d182-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="9d182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d182-102">SYNOPSIS</span></span>
<span data-ttu-id="9d182-103">Yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9d182-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d182-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d182-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d182-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d182-105">DESCRIPTION</span></span>
<span data-ttu-id="9d182-106">**Get-AzureRmRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9d182-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="9d182-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d182-107">EXAMPLES</span></span>

### <span data-ttu-id="9d182-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9d182-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="9d182-109">Kasa için yedek kasa özelliğini edinin.</span><span class="sxs-lookup"><span data-stu-id="9d182-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="9d182-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d182-110">PARAMETERS</span></span>

### <span data-ttu-id="9d182-111">-Kasa</span><span class="sxs-lookup"><span data-stu-id="9d182-111">-Vault</span></span>
<span data-ttu-id="9d182-112">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d182-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="9d182-113">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d182-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d182-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d182-114">-DefaultProfile</span></span>
<span data-ttu-id="9d182-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d182-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d182-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d182-116">CommonParameters</span></span>
<span data-ttu-id="9d182-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d182-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d182-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d182-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d182-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d182-119">INPUTS</span></span>

### <span data-ttu-id="9d182-120">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="9d182-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="9d182-121">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d182-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="9d182-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d182-122">OUTPUTS</span></span>

### <span data-ttu-id="9d182-123">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="9d182-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="9d182-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d182-124">NOTES</span></span>

## <span data-ttu-id="9d182-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d182-125">RELATED LINKS</span></span>
