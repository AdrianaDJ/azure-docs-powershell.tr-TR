---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103541"
---
# <span data-ttu-id="0441f-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0441f-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="0441f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0441f-102">SYNOPSIS</span></span>
<span data-ttu-id="0441f-103">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="0441f-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0441f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0441f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0441f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0441f-105">DESCRIPTION</span></span>
<span data-ttu-id="0441f-106">**Remove-Azrecoveryserviceskasa** cmdlet 'ı bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="0441f-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0441f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0441f-107">EXAMPLES</span></span>

### <span data-ttu-id="0441f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0441f-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="0441f-109">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="0441f-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="0441f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0441f-110">PARAMETERS</span></span>

### <span data-ttu-id="0441f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0441f-111">-DefaultProfile</span></span>
<span data-ttu-id="0441f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0441f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0441f-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="0441f-113">-Vault</span></span>
<span data-ttu-id="0441f-114">Bir Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0441f-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="0441f-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="0441f-115">-Confirm</span></span>
<span data-ttu-id="0441f-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0441f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0441f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0441f-117">-WhatIf</span></span>
<span data-ttu-id="0441f-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0441f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0441f-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0441f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0441f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0441f-120">CommonParameters</span></span>
<span data-ttu-id="0441f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0441f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0441f-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0441f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0441f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0441f-123">INPUTS</span></span>

### <span data-ttu-id="0441f-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="0441f-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0441f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0441f-125">OUTPUTS</span></span>

### <span data-ttu-id="0441f-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput çıkışı</span><span class="sxs-lookup"><span data-stu-id="0441f-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="0441f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0441f-127">NOTES</span></span>

## <span data-ttu-id="0441f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0441f-128">RELATED LINKS</span></span>

[<span data-ttu-id="0441f-129">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="0441f-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="0441f-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0441f-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0441f-131">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="0441f-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


