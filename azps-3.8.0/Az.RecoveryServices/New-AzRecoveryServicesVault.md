---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098161"
---
# <span data-ttu-id="ca9df-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ca9df-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="ca9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9df-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9df-103">Yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca9df-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="ca9df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca9df-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca9df-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9df-106">**Yeni-Azrecoveryserviceskasa** cmdlet 'i yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca9df-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="ca9df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca9df-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9df-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca9df-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="ca9df-109">Kaynak grubunda ve verilen konumda kurtarma hizmeti Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca9df-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="ca9df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca9df-110">PARAMETERS</span></span>

### <span data-ttu-id="ca9df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9df-111">-DefaultProfile</span></span>
<span data-ttu-id="ca9df-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca9df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca9df-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca9df-113">-Location</span></span>
<span data-ttu-id="ca9df-114">Kasanın coğrafi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca9df-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="ca9df-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca9df-115">-Name</span></span>
<span data-ttu-id="ca9df-116">Oluşturulacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca9df-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="ca9df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9df-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca9df-118">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca9df-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="ca9df-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ca9df-119">-Tag</span></span>

<span data-ttu-id="ca9df-120">Kurtarma Hizmetleri kasasına eklenecek etiketleri belirtir</span><span class="sxs-lookup"><span data-stu-id="ca9df-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9df-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca9df-121">-Confirm</span></span>
<span data-ttu-id="ca9df-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca9df-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9df-123">-WhatIf</span></span>
<span data-ttu-id="ca9df-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca9df-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca9df-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca9df-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9df-126">CommonParameters</span></span>
<span data-ttu-id="ca9df-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca9df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9df-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca9df-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9df-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca9df-129">INPUTS</span></span>

### <span data-ttu-id="ca9df-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ca9df-130">None</span></span>

## <span data-ttu-id="ca9df-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca9df-131">OUTPUTS</span></span>

### <span data-ttu-id="ca9df-132">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="ca9df-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ca9df-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca9df-133">NOTES</span></span>

## <span data-ttu-id="ca9df-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca9df-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca9df-135">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="ca9df-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ca9df-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ca9df-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ca9df-137">Remove-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="ca9df-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


