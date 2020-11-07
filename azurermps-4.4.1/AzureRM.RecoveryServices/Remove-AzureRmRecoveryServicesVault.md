---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763640"
---
# <span data-ttu-id="158ed-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="158ed-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="158ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158ed-102">SYNOPSIS</span></span>
<span data-ttu-id="158ed-103">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="158ed-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="158ed-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="158ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="158ed-105">DESCRIPTION</span></span>
<span data-ttu-id="158ed-106">**Remove-Azurermrecoveryserviceskasası**</span><span class="sxs-lookup"><span data-stu-id="158ed-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="158ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="158ed-107">EXAMPLES</span></span>

## <span data-ttu-id="158ed-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="158ed-108">PARAMETERS</span></span>

### <span data-ttu-id="158ed-109">-Kasa</span><span class="sxs-lookup"><span data-stu-id="158ed-109">-Vault</span></span>
<span data-ttu-id="158ed-110">Bir Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="158ed-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="158ed-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="158ed-111">-Confirm</span></span>
<span data-ttu-id="158ed-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="158ed-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158ed-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158ed-113">-WhatIf</span></span>
<span data-ttu-id="158ed-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="158ed-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="158ed-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="158ed-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158ed-116">-DefaultProfile</span></span>
<span data-ttu-id="158ed-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="158ed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158ed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158ed-118">CommonParameters</span></span>
<span data-ttu-id="158ed-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="158ed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158ed-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158ed-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158ed-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="158ed-121">INPUTS</span></span>

### <span data-ttu-id="158ed-122">Arskasa</span><span class="sxs-lookup"><span data-stu-id="158ed-122">ARSVault</span></span>
<span data-ttu-id="158ed-123">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="158ed-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="158ed-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="158ed-124">OUTPUTS</span></span>

### <span data-ttu-id="158ed-125">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput çıkışı</span><span class="sxs-lookup"><span data-stu-id="158ed-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="158ed-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="158ed-126">NOTES</span></span>

## <span data-ttu-id="158ed-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="158ed-127">RELATED LINKS</span></span>

[<span data-ttu-id="158ed-128">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="158ed-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="158ed-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="158ed-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="158ed-130">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="158ed-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


