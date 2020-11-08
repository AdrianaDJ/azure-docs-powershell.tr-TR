---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277210"
---
# <span data-ttu-id="6b62f-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="6b62f-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="6b62f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b62f-102">SYNOPSIS</span></span>

<span data-ttu-id="6b62f-103">Kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b62f-103">Sets vault context.</span></span>

## <span data-ttu-id="6b62f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b62f-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b62f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b62f-105">DESCRIPTION</span></span>

<span data-ttu-id="6b62f-106">**Set-AzRecoveryServicesVaultContext** cmdlet 'ı Azure Site Recovery Hizmetleri için kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b62f-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="6b62f-107">Uyarı: Bu cmdlet gelecekteki bir son değişiklik sürümünde kullanım dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="6b62f-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="6b62f-108">Yerine geçmez.</span><span class="sxs-lookup"><span data-stu-id="6b62f-108">There will be no replacement for it.</span></span> <span data-ttu-id="6b62f-109">Lütfen ileri gelen tüm kurtarma hizmetleri komutlarında-VaultId parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6b62f-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="6b62f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b62f-110">EXAMPLES</span></span>

### <span data-ttu-id="6b62f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6b62f-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="6b62f-112">Kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b62f-112">Sets vault context.</span></span>

## <span data-ttu-id="6b62f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b62f-113">PARAMETERS</span></span>

### <span data-ttu-id="6b62f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b62f-114">-DefaultProfile</span></span>

<span data-ttu-id="6b62f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b62f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b62f-116">-Kasa</span><span class="sxs-lookup"><span data-stu-id="6b62f-116">-Vault</span></span>

<span data-ttu-id="6b62f-117">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b62f-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="6b62f-118">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b62f-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="6b62f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b62f-119">CommonParameters</span></span>
<span data-ttu-id="6b62f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b62f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b62f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b62f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b62f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b62f-122">INPUTS</span></span>

### <span data-ttu-id="6b62f-123">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="6b62f-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6b62f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b62f-124">OUTPUTS</span></span>

### <span data-ttu-id="6b62f-125">System. void</span><span class="sxs-lookup"><span data-stu-id="6b62f-125">System.Void</span></span>

## <span data-ttu-id="6b62f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b62f-126">NOTES</span></span>

## <span data-ttu-id="6b62f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b62f-127">RELATED LINKS</span></span>
