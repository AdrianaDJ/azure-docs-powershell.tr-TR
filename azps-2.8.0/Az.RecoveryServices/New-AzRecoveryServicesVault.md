---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933482"
---
# <span data-ttu-id="f55a2-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f55a2-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f55a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f55a2-103">Yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f55a2-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f55a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f55a2-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f55a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f55a2-106">**Yeni-Azrecoveryserviceskasa** cmdlet 'i yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f55a2-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f55a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f55a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f55a2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f55a2-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="f55a2-109">Kaynak grubunda ve verilen konumda kurtarma hizmeti Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f55a2-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="f55a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f55a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f55a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55a2-111">-DefaultProfile</span></span>
<span data-ttu-id="f55a2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f55a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f55a2-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="f55a2-113">-Location</span></span>
<span data-ttu-id="f55a2-114">Kasanın coğrafi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f55a2-114">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f55a2-115">-Name</span></span>
<span data-ttu-id="f55a2-116">Oluşturulacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f55a2-116">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="f55a2-118">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f55a2-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f55a2-119">-Confirm</span></span>
<span data-ttu-id="f55a2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f55a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55a2-121">-WhatIf</span></span>
<span data-ttu-id="f55a2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f55a2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f55a2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f55a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55a2-124">CommonParameters</span></span>
<span data-ttu-id="f55a2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f55a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55a2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55a2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f55a2-127">INPUTS</span></span>

### <span data-ttu-id="f55a2-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f55a2-128">None</span></span>

## <span data-ttu-id="f55a2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f55a2-129">OUTPUTS</span></span>

### <span data-ttu-id="f55a2-130">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="f55a2-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f55a2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f55a2-131">NOTES</span></span>

## <span data-ttu-id="f55a2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f55a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="f55a2-133">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="f55a2-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f55a2-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f55a2-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f55a2-135">Remove-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="f55a2-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


