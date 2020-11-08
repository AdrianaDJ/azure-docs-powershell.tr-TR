---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098999"
---
# <span data-ttu-id="83789-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="83789-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="83789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83789-102">SYNOPSIS</span></span>
<span data-ttu-id="83789-103">Kasanın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83789-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="83789-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83789-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83789-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83789-105">DESCRIPTION</span></span>
<span data-ttu-id="83789-106">**Set-AzRecoveryServicesVaultProperty** cmdlet 'i, bir kurtarma hizmetleri Kasası 'nın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83789-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="83789-107">Bir kasanın geçerli özelliklerini almak için **set-AzRecoveryServicesVaultProperty** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83789-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="83789-108">Bu **cmdlet 'i** kullanma bir kasaın herhangi bir noktasında etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="83789-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="83789-109">Bir kasaya ait **Softdeletefeaturestate** özelliği, yalnızca kasada hiç kaydettirilmiş kapsayıcı yoksa devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="83789-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="83789-110">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83789-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="83789-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83789-111">EXAMPLES</span></span>

### <span data-ttu-id="83789-112">Örnek 1: bir kasaya yönelik güncelleştirme yazılım</span><span class="sxs-lookup"><span data-stu-id="83789-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="83789-113">İlk komut bir kasa nesnesi alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="83789-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="83789-114">İkinci komut, kasadaki SoftDeleteFeatureState özelliğini "Enabled" durumuna günceller.</span><span class="sxs-lookup"><span data-stu-id="83789-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="83789-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83789-115">PARAMETERS</span></span>

### <span data-ttu-id="83789-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83789-116">-DefaultProfile</span></span>
<span data-ttu-id="83789-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83789-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83789-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="83789-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="83789-119">Softdeletefeaturesk</span><span class="sxs-lookup"><span data-stu-id="83789-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="83789-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="83789-120">-VaultId</span></span>
<span data-ttu-id="83789-121">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83789-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="83789-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="83789-122">-Confirm</span></span>
<span data-ttu-id="83789-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83789-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83789-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83789-124">-WhatIf</span></span>
<span data-ttu-id="83789-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83789-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83789-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83789-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83789-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83789-127">CommonParameters</span></span>
<span data-ttu-id="83789-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83789-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83789-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83789-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83789-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83789-130">INPUTS</span></span>

### <span data-ttu-id="83789-131">System. String</span><span class="sxs-lookup"><span data-stu-id="83789-131">System.String</span></span>

### <span data-ttu-id="83789-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="83789-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="83789-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83789-133">OUTPUTS</span></span>

### <span data-ttu-id="83789-134">Microsoft. Azure. Management. RecoveryServices. Backup. modeller. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="83789-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="83789-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83789-135">NOTES</span></span>

## <span data-ttu-id="83789-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83789-136">RELATED LINKS</span></span>

[<span data-ttu-id="83789-137">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="83789-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="83789-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="83789-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


