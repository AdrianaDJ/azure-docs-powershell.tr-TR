---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274245"
---
# <span data-ttu-id="fbe32-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="fbe32-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="fbe32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe32-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe32-103">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="fbe32-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="fbe32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbe32-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe32-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbe32-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe32-106">**Remove-Azrecoveryserviceskasa** cmdlet 'ı bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="fbe32-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="fbe32-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbe32-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe32-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fbe32-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="fbe32-109">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="fbe32-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="fbe32-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbe32-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe32-111">-DefaultProfile</span></span>
<span data-ttu-id="fbe32-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbe32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe32-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="fbe32-113">-Vault</span></span>
<span data-ttu-id="fbe32-114">Bir Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe32-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="fbe32-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbe32-115">-Confirm</span></span>
<span data-ttu-id="fbe32-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbe32-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe32-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe32-117">-WhatIf</span></span>
<span data-ttu-id="fbe32-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbe32-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbe32-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbe32-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe32-120">CommonParameters</span></span>
<span data-ttu-id="fbe32-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbe32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe32-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fbe32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe32-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbe32-123">INPUTS</span></span>

### <span data-ttu-id="fbe32-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="fbe32-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="fbe32-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbe32-125">OUTPUTS</span></span>

### <span data-ttu-id="fbe32-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput çıkışı</span><span class="sxs-lookup"><span data-stu-id="fbe32-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="fbe32-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbe32-127">NOTES</span></span>

## <span data-ttu-id="fbe32-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbe32-128">RELATED LINKS</span></span>

[<span data-ttu-id="fbe32-129">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="fbe32-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="fbe32-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fbe32-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="fbe32-131">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="fbe32-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


