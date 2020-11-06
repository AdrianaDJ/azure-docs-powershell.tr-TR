---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587814"
---
# <span data-ttu-id="496d8-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="496d8-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="496d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496d8-102">SYNOPSIS</span></span>
<span data-ttu-id="496d8-103">Yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="496d8-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="496d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="496d8-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="496d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="496d8-105">DESCRIPTION</span></span>
<span data-ttu-id="496d8-106">**Yeni-Azurermrecoveryserviceskasa** cmdlet 'i yeni bir kurtarma hizmetleri Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="496d8-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="496d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="496d8-107">EXAMPLES</span></span>

## <span data-ttu-id="496d8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="496d8-108">PARAMETERS</span></span>

### <span data-ttu-id="496d8-109">-Konum</span><span class="sxs-lookup"><span data-stu-id="496d8-109">-Location</span></span>
<span data-ttu-id="496d8-110">Kasanın coğrafi konumunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="496d8-110">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="496d8-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="496d8-111">-Name</span></span>
<span data-ttu-id="496d8-112">Oluşturulacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="496d8-112">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="496d8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496d8-113">-ResourceGroupName</span></span>
<span data-ttu-id="496d8-114">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="496d8-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="496d8-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="496d8-115">-Confirm</span></span>
<span data-ttu-id="496d8-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="496d8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496d8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496d8-117">-WhatIf</span></span>
<span data-ttu-id="496d8-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="496d8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="496d8-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="496d8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496d8-120">-DefaultProfile</span></span>
<span data-ttu-id="496d8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="496d8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="496d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496d8-122">CommonParameters</span></span>
<span data-ttu-id="496d8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="496d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496d8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496d8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496d8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="496d8-125">INPUTS</span></span>

## <span data-ttu-id="496d8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="496d8-126">OUTPUTS</span></span>

### <span data-ttu-id="496d8-127">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="496d8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="496d8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="496d8-128">NOTES</span></span>

## <span data-ttu-id="496d8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="496d8-129">RELATED LINKS</span></span>

[<span data-ttu-id="496d8-130">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="496d8-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="496d8-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="496d8-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="496d8-132">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="496d8-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


