---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592926"
---
# <span data-ttu-id="280e4-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="280e4-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="280e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="280e4-102">SYNOPSIS</span></span>
<span data-ttu-id="280e4-103">Kurtarma Hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="280e4-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="280e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="280e4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="280e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="280e4-105">DESCRIPTION</span></span>
<span data-ttu-id="280e4-106">**Get-Azurermrecoveryserviceskasa** cmdlet 'i geçerli abonelikteki kurtarma hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="280e4-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="280e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="280e4-107">EXAMPLES</span></span>

### <span data-ttu-id="280e4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="280e4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="280e4-109">Seçili abonelikteki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="280e4-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="280e4-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="280e4-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="280e4-111">Seçili abonelikteki kaynak grubundaki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="280e4-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="280e4-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="280e4-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="280e4-113">Kaynak grubundaki kasayı verilen adla edinin.</span><span class="sxs-lookup"><span data-stu-id="280e4-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="280e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="280e4-114">PARAMETERS</span></span>

### <span data-ttu-id="280e4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="280e4-115">-Name</span></span>
<span data-ttu-id="280e4-116">Sorgulanacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="280e4-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="280e4-118">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı veya alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="280e4-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280e4-119">-DefaultProfile</span></span>
<span data-ttu-id="280e4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="280e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="280e4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280e4-121">CommonParameters</span></span>
<span data-ttu-id="280e4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="280e4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280e4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="280e4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280e4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="280e4-124">INPUTS</span></span>

### <span data-ttu-id="280e4-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="280e4-125">None</span></span>
<span data-ttu-id="280e4-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="280e4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="280e4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="280e4-127">OUTPUTS</span></span>

### <span data-ttu-id="280e4-128">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. RecoveryServices. Arskasa]</span><span class="sxs-lookup"><span data-stu-id="280e4-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="280e4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="280e4-129">NOTES</span></span>

## <span data-ttu-id="280e4-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="280e4-130">RELATED LINKS</span></span>

[<span data-ttu-id="280e4-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="280e4-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="280e4-132">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="280e4-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="280e4-133">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="280e4-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


