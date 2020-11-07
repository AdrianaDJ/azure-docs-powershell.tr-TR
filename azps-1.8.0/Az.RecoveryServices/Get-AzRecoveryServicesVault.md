---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759681"
---
# <span data-ttu-id="cb9d7-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cb9d7-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="cb9d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9d7-103">Kurtarma Hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="cb9d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb9d7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb9d7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9d7-106">**Get-Azrecoveryserviceskasa** cmdlet 'i geçerli abonelikteki kurtarma hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="cb9d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb9d7-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9d7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb9d7-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="cb9d7-109">Seçili abonelikteki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="cb9d7-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cb9d7-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="cb9d7-111">Seçili abonelikteki kaynak grubundaki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="cb9d7-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cb9d7-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="cb9d7-113">Kaynak grubundaki kasayı verilen adla edinin.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="cb9d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb9d7-114">PARAMETERS</span></span>

### <span data-ttu-id="cb9d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9d7-115">-DefaultProfile</span></span>
<span data-ttu-id="cb9d7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9d7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb9d7-117">-Name</span></span>
<span data-ttu-id="cb9d7-118">Sorgulanacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="cb9d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb9d7-120">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="cb9d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9d7-121">CommonParameters</span></span>
<span data-ttu-id="cb9d7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb9d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9d7-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9d7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9d7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb9d7-124">INPUTS</span></span>

### <span data-ttu-id="cb9d7-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb9d7-125">None</span></span>

## <span data-ttu-id="cb9d7-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb9d7-126">OUTPUTS</span></span>

### <span data-ttu-id="cb9d7-127">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="cb9d7-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="cb9d7-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb9d7-128">NOTES</span></span>

## <span data-ttu-id="cb9d7-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb9d7-129">RELATED LINKS</span></span>

[<span data-ttu-id="cb9d7-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cb9d7-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="cb9d7-131">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="cb9d7-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="cb9d7-132">Remove-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="cb9d7-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


