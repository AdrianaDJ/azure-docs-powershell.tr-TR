---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592422"
---
# <span data-ttu-id="7b167-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7b167-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="7b167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b167-102">SYNOPSIS</span></span>
<span data-ttu-id="7b167-103">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="7b167-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b167-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b167-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b167-105">DESCRIPTION</span></span>
<span data-ttu-id="7b167-106">**Remove-Azurermrecoveryserviceskasası**</span><span class="sxs-lookup"><span data-stu-id="7b167-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7b167-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b167-107">EXAMPLES</span></span>

### <span data-ttu-id="7b167-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b167-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="7b167-109">Bir kurtarma hizmetleri Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="7b167-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7b167-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b167-110">PARAMETERS</span></span>

### <span data-ttu-id="7b167-111">-Kasa</span><span class="sxs-lookup"><span data-stu-id="7b167-111">-Vault</span></span>
<span data-ttu-id="7b167-112">Bir Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b167-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="7b167-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b167-113">-Confirm</span></span>
<span data-ttu-id="7b167-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b167-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b167-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b167-115">-WhatIf</span></span>
<span data-ttu-id="7b167-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b167-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b167-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b167-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b167-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b167-118">-DefaultProfile</span></span>
<span data-ttu-id="7b167-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b167-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b167-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b167-120">CommonParameters</span></span>
<span data-ttu-id="7b167-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b167-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b167-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b167-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b167-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b167-123">INPUTS</span></span>

### <span data-ttu-id="7b167-124">Arskasa</span><span class="sxs-lookup"><span data-stu-id="7b167-124">ARSVault</span></span>
<span data-ttu-id="7b167-125">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7b167-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="7b167-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b167-126">OUTPUTS</span></span>

### <span data-ttu-id="7b167-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput çıkışı</span><span class="sxs-lookup"><span data-stu-id="7b167-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="7b167-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b167-128">NOTES</span></span>

## <span data-ttu-id="7b167-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b167-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b167-130">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="7b167-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7b167-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7b167-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7b167-132">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="7b167-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


