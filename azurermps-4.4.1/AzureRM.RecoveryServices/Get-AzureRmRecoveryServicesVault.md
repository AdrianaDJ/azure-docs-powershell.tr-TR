---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593028"
---
# <span data-ttu-id="1345e-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1345e-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="1345e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1345e-102">SYNOPSIS</span></span>
<span data-ttu-id="1345e-103">Kurtarma Hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1345e-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1345e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1345e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1345e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1345e-105">DESCRIPTION</span></span>
<span data-ttu-id="1345e-106">**Get-Azurermrecoveryserviceskasa** cmdlet 'i geçerli abonelikteki kurtarma hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1345e-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="1345e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1345e-107">EXAMPLES</span></span>

## <span data-ttu-id="1345e-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1345e-108">PARAMETERS</span></span>

### <span data-ttu-id="1345e-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="1345e-109">-Name</span></span>
<span data-ttu-id="1345e-110">Sorgulanacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1345e-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1345e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1345e-111">-ResourceGroupName</span></span>
<span data-ttu-id="1345e-112">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1345e-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1345e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1345e-113">-DefaultProfile</span></span>
<span data-ttu-id="1345e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1345e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1345e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1345e-115">CommonParameters</span></span>
<span data-ttu-id="1345e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1345e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1345e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1345e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1345e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1345e-118">INPUTS</span></span>

## <span data-ttu-id="1345e-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1345e-119">OUTPUTS</span></span>

### <span data-ttu-id="1345e-120">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. RecoveryServices. Arskasa]</span><span class="sxs-lookup"><span data-stu-id="1345e-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="1345e-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1345e-121">NOTES</span></span>

## <span data-ttu-id="1345e-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1345e-122">RELATED LINKS</span></span>

[<span data-ttu-id="1345e-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1345e-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="1345e-124">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="1345e-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="1345e-125">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="1345e-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


