---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 3abb13803dbe564eb7562691b10a453174374444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592918"
---
# <span data-ttu-id="9aecf-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9aecf-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="9aecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aecf-102">SYNOPSIS</span></span>
<span data-ttu-id="9aecf-103">Yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9aecf-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aecf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9aecf-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aecf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9aecf-105">DESCRIPTION</span></span>
<span data-ttu-id="9aecf-106">**Yeni-Azurermrecoveryserviceskasa** cmdlet 'i yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9aecf-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="9aecf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9aecf-107">EXAMPLES</span></span>

### <span data-ttu-id="9aecf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9aecf-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="9aecf-109">Kaynak grubunda ve verilen konumda kurtarma hizmeti Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9aecf-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="9aecf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9aecf-110">PARAMETERS</span></span>

### <span data-ttu-id="9aecf-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="9aecf-111">-Location</span></span>
<span data-ttu-id="9aecf-112">Kasanın coğrafi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9aecf-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aecf-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9aecf-113">-Name</span></span>
<span data-ttu-id="9aecf-114">Oluşturulacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9aecf-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aecf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aecf-115">-ResourceGroupName</span></span>
<span data-ttu-id="9aecf-116">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9aecf-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aecf-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9aecf-117">-Confirm</span></span>
<span data-ttu-id="9aecf-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9aecf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aecf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aecf-119">-WhatIf</span></span>
<span data-ttu-id="9aecf-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9aecf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aecf-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9aecf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aecf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aecf-122">-DefaultProfile</span></span>
<span data-ttu-id="9aecf-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9aecf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aecf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aecf-124">CommonParameters</span></span>
<span data-ttu-id="9aecf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9aecf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aecf-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aecf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aecf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9aecf-127">INPUTS</span></span>

### <span data-ttu-id="9aecf-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9aecf-128">None</span></span>
<span data-ttu-id="9aecf-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9aecf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9aecf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9aecf-130">OUTPUTS</span></span>

### <span data-ttu-id="9aecf-131">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="9aecf-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9aecf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9aecf-132">NOTES</span></span>

## <span data-ttu-id="9aecf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9aecf-133">RELATED LINKS</span></span>

[<span data-ttu-id="9aecf-134">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="9aecf-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="9aecf-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9aecf-135">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9aecf-136">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="9aecf-136">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)

