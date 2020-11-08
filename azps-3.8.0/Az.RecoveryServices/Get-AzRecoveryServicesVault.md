---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104716"
---
# <span data-ttu-id="2155d-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2155d-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="2155d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2155d-102">SYNOPSIS</span></span>

<span data-ttu-id="2155d-103">Kurtarma Hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2155d-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="2155d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2155d-104">SYNTAX</span></span>

### <span data-ttu-id="2155d-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="2155d-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2155d-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2155d-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2155d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2155d-107">DESCRIPTION</span></span>

<span data-ttu-id="2155d-108">**Get-Azrecoveryserviceskasa** cmdlet 'i geçerli abonelikteki kurtarma hizmetleri 'nin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2155d-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="2155d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2155d-109">EXAMPLES</span></span>

### <span data-ttu-id="2155d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2155d-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="2155d-111">Seçili abonelikteki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2155d-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="2155d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2155d-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="2155d-113">Seçili abonelikteki kaynak grubundaki kasa listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2155d-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="2155d-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2155d-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="2155d-115">Kaynak grubundaki kasayı verilen adla edinin.</span><span class="sxs-lookup"><span data-stu-id="2155d-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="2155d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2155d-116">PARAMETERS</span></span>

### <span data-ttu-id="2155d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2155d-117">-DefaultProfile</span></span>

<span data-ttu-id="2155d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2155d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2155d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2155d-119">-Name</span></span>

<span data-ttu-id="2155d-120">Sorgulanacak kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2155d-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2155d-121">-ResourceGroupName</span></span>

<span data-ttu-id="2155d-122">Belirtilen Kurtarma Hizmetleri nesnesinin alınacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2155d-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155d-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2155d-123">-Tag</span></span>

<span data-ttu-id="2155d-124">Sorgulanacak etiketleri belirtir</span><span class="sxs-lookup"><span data-stu-id="2155d-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155d-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="2155d-125">-TagName</span></span>

<span data-ttu-id="2155d-126">Sorgulanacak etiketin anahtarını belirtir</span><span class="sxs-lookup"><span data-stu-id="2155d-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155d-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="2155d-127">-TagValue</span></span>

<span data-ttu-id="2155d-128">Sorgulanacak etiketin değerini belirtir</span><span class="sxs-lookup"><span data-stu-id="2155d-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2155d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2155d-129">CommonParameters</span></span>
<span data-ttu-id="2155d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2155d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2155d-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2155d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2155d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2155d-132">INPUTS</span></span>

### <span data-ttu-id="2155d-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2155d-133">None</span></span>

## <span data-ttu-id="2155d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2155d-134">OUTPUTS</span></span>

### <span data-ttu-id="2155d-135">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="2155d-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="2155d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2155d-136">NOTES</span></span>

## <span data-ttu-id="2155d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2155d-137">RELATED LINKS</span></span>

[<span data-ttu-id="2155d-138">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2155d-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="2155d-139">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="2155d-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="2155d-140">Remove-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="2155d-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
