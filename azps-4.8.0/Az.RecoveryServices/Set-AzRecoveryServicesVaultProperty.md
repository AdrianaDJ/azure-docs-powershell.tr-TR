---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274013"
---
# <span data-ttu-id="fd755-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="fd755-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="fd755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd755-102">SYNOPSIS</span></span>
<span data-ttu-id="fd755-103">Kasanın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd755-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="fd755-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd755-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd755-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd755-105">DESCRIPTION</span></span>
<span data-ttu-id="fd755-106">**Set-AzRecoveryServicesVaultProperty** cmdlet 'i, bir kurtarma hizmetleri Kasası 'nın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd755-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="fd755-107">Bu cmdlet, geçerli küme işleminden sonraki güncelleştirilmiş kasa özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd755-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="fd755-108">Örneğin, yumuşak silme gibi kasa 'nın bu cmdlet özelliklerini kullanmak, herhangi bir zamanda etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fd755-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="fd755-109">Bir kasaya ait **Softdeletefeaturestate** özelliği, yalnızca kasada hiç kaydettirilmiş kapsayıcı yoksa devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="fd755-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="fd755-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd755-110">EXAMPLES</span></span>

### <span data-ttu-id="fd755-111">Örnek 1: bir kasaya yönelik güncelleştirme yazılım</span><span class="sxs-lookup"><span data-stu-id="fd755-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="fd755-112">İlk komut bir kasa nesnesi alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fd755-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="fd755-113">İkinci komut, kasadaki SoftDeleteFeatureState özelliğini "Enabled" durumuna günceller.</span><span class="sxs-lookup"><span data-stu-id="fd755-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="fd755-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd755-114">PARAMETERS</span></span>

### <span data-ttu-id="fd755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd755-115">-DefaultProfile</span></span>
<span data-ttu-id="fd755-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd755-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd755-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="fd755-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="fd755-118">Softdeletefeaturesk</span><span class="sxs-lookup"><span data-stu-id="fd755-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd755-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fd755-119">-VaultId</span></span>
<span data-ttu-id="fd755-120">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fd755-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd755-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd755-121">-Confirm</span></span>
<span data-ttu-id="fd755-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd755-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd755-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd755-123">-WhatIf</span></span>
<span data-ttu-id="fd755-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd755-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="fd755-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd755-125">CommonParameters</span></span>
<span data-ttu-id="fd755-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd755-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd755-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd755-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd755-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd755-128">INPUTS</span></span>

### <span data-ttu-id="fd755-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fd755-129">System.String</span></span>

### <span data-ttu-id="fd755-130">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="fd755-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="fd755-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd755-131">OUTPUTS</span></span>

### <span data-ttu-id="fd755-132">Microsoft. Azure. Management. RecoveryServices. Backup. modeller. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="fd755-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="fd755-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd755-133">NOTES</span></span>

## <span data-ttu-id="fd755-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd755-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd755-135">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="fd755-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="fd755-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="fd755-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


