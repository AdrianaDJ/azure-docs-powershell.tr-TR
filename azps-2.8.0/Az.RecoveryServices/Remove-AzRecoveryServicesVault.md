---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932965"
---
# <span data-ttu-id="5fbf5-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5fbf5-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="5fbf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbf5-103">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="5fbf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fbf5-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fbf5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fbf5-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbf5-106">**Remove-Azrecoveryserviceskasa** cmdlet 'ı bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="5fbf5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fbf5-107">EXAMPLES</span></span>

### <span data-ttu-id="5fbf5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5fbf5-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="5fbf5-109">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="5fbf5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fbf5-110">PARAMETERS</span></span>

### <span data-ttu-id="5fbf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbf5-111">-DefaultProfile</span></span>
<span data-ttu-id="5fbf5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fbf5-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="5fbf5-113">-Vault</span></span>
<span data-ttu-id="5fbf5-114">Bir Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="5fbf5-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fbf5-115">-Confirm</span></span>
<span data-ttu-id="5fbf5-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbf5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbf5-117">-WhatIf</span></span>
<span data-ttu-id="5fbf5-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fbf5-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbf5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbf5-120">CommonParameters</span></span>
<span data-ttu-id="5fbf5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fbf5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbf5-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbf5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbf5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fbf5-123">INPUTS</span></span>

### <span data-ttu-id="5fbf5-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="5fbf5-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="5fbf5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fbf5-125">OUTPUTS</span></span>

### <span data-ttu-id="5fbf5-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput çıkışı</span><span class="sxs-lookup"><span data-stu-id="5fbf5-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="5fbf5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fbf5-127">NOTES</span></span>

## <span data-ttu-id="5fbf5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fbf5-128">RELATED LINKS</span></span>

[<span data-ttu-id="5fbf5-129">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="5fbf5-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="5fbf5-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5fbf5-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="5fbf5-131">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="5fbf5-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

