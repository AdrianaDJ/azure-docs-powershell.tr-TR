---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764250"
---
# <span data-ttu-id="889c0-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="889c0-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="889c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="889c0-102">SYNOPSIS</span></span>
<span data-ttu-id="889c0-103">Kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="889c0-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="889c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="889c0-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="889c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="889c0-105">DESCRIPTION</span></span>
<span data-ttu-id="889c0-106">**Set-AzureRmRecoveryServicesVaultContext** cmdlet 'ı Azure Site Recovery Services için kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="889c0-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="889c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="889c0-107">EXAMPLES</span></span>

## <span data-ttu-id="889c0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="889c0-108">PARAMETERS</span></span>

### <span data-ttu-id="889c0-109">-Kasa</span><span class="sxs-lookup"><span data-stu-id="889c0-109">-Vault</span></span>
<span data-ttu-id="889c0-110">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="889c0-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="889c0-111">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="889c0-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="889c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889c0-112">-DefaultProfile</span></span>
<span data-ttu-id="889c0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="889c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="889c0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889c0-114">CommonParameters</span></span>
<span data-ttu-id="889c0-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="889c0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889c0-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889c0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889c0-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="889c0-117">INPUTS</span></span>

### <span data-ttu-id="889c0-118">Arskasa</span><span class="sxs-lookup"><span data-stu-id="889c0-118">ARSVault</span></span>
<span data-ttu-id="889c0-119">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="889c0-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="889c0-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="889c0-120">OUTPUTS</span></span>

## <span data-ttu-id="889c0-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="889c0-121">NOTES</span></span>

## <span data-ttu-id="889c0-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="889c0-122">RELATED LINKS</span></span>

