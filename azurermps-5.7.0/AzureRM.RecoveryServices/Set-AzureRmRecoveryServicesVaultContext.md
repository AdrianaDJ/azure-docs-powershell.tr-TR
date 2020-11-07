---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763244"
---
# <span data-ttu-id="9154f-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9154f-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9154f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9154f-102">SYNOPSIS</span></span>
<span data-ttu-id="9154f-103">Kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9154f-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9154f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9154f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9154f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9154f-105">DESCRIPTION</span></span>
<span data-ttu-id="9154f-106">**Set-AzureRmRecoveryServicesVaultContext** cmdlet 'ı Azure Site Recovery Services için kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9154f-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="9154f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9154f-107">EXAMPLES</span></span>

### <span data-ttu-id="9154f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9154f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9154f-109">Kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9154f-109">Sets vault context.</span></span>

## <span data-ttu-id="9154f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9154f-110">PARAMETERS</span></span>

### <span data-ttu-id="9154f-111">-Kasa</span><span class="sxs-lookup"><span data-stu-id="9154f-111">-Vault</span></span>
<span data-ttu-id="9154f-112">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9154f-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="9154f-113">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9154f-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9154f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9154f-114">-DefaultProfile</span></span>
<span data-ttu-id="9154f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9154f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9154f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9154f-116">CommonParameters</span></span>
<span data-ttu-id="9154f-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9154f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9154f-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9154f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9154f-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9154f-119">INPUTS</span></span>

### <span data-ttu-id="9154f-120">Arskasa</span><span class="sxs-lookup"><span data-stu-id="9154f-120">ARSVault</span></span>
<span data-ttu-id="9154f-121">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9154f-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="9154f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9154f-122">OUTPUTS</span></span>

## <span data-ttu-id="9154f-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9154f-123">NOTES</span></span>

## <span data-ttu-id="9154f-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9154f-124">RELATED LINKS</span></span>

