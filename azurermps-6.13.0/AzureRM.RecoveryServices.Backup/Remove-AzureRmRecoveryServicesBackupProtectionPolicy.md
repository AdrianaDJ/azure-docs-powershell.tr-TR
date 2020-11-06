---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 805deece859eb4baa05d8c3d34dfcc8a9d571354
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594344"
---
# <span data-ttu-id="d18c0-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18c0-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d18c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d18c0-103">Bir kasadan yedek koruma ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="d18c0-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d18c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d18c0-104">SYNTAX</span></span>

### <span data-ttu-id="d18c0-105">PolicyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d18c0-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d18c0-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="d18c0-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18c0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d18c0-107">DESCRIPTION</span></span>
<span data-ttu-id="d18c0-108">**Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'inin yedekleme ilkelerini siler.</span><span class="sxs-lookup"><span data-stu-id="d18c0-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="d18c0-109">Yedekleme koruma ilkesini silebilmeniz için, ilkenin ilişkili yedekleme öğeleri olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d18c0-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="d18c0-110">İlkeyi silmeden önce, her ilişkili öğenin başka bir ilkeyle ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d18c0-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="d18c0-111">Başka bir ilkeyi yedekleme öğesiyle ilişkilendirmek için Enable-AzureRmRecoveryServicesBackupProtection cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d18c0-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="d18c0-112">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d18c0-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d18c0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d18c0-113">EXAMPLES</span></span>

### <span data-ttu-id="d18c0-114">Örnek 1: ilkeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="d18c0-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="d18c0-115">İlk komut NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d18c0-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d18c0-116">İkinci komut $Pol ilke nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d18c0-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="d18c0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d18c0-117">PARAMETERS</span></span>

### <span data-ttu-id="d18c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18c0-118">-DefaultProfile</span></span>
<span data-ttu-id="d18c0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d18c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18c0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d18c0-120">-Force</span></span>
<span data-ttu-id="d18c0-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d18c0-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d18c0-122">-Name</span></span>
<span data-ttu-id="d18c0-123">Kaldırılacak yedekleme koruması ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d18c0-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d18c0-124">-PassThru</span></span>
<span data-ttu-id="d18c0-125">Silinecek ilkeyi döndür.</span><span class="sxs-lookup"><span data-stu-id="d18c0-125">Return the policy to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-126">-İlke</span><span class="sxs-lookup"><span data-stu-id="d18c0-126">-Policy</span></span>
<span data-ttu-id="d18c0-127">Kaldırılacak yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d18c0-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="d18c0-128">**Yedeklemeilkesi** nesnesi almak için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d18c0-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d18c0-129">-VaultId</span></span>
<span data-ttu-id="d18c0-130">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d18c0-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d18c0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d18c0-131">-Confirm</span></span>
<span data-ttu-id="d18c0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d18c0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18c0-133">-WhatIf</span></span>
<span data-ttu-id="d18c0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d18c0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18c0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d18c0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18c0-136">CommonParameters</span></span>
<span data-ttu-id="d18c0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d18c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18c0-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18c0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18c0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d18c0-139">INPUTS</span></span>

### <span data-ttu-id="d18c0-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d18c0-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="d18c0-141">Parametreler: Ilke (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d18c0-141">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="d18c0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d18c0-142">System.String</span></span>
<span data-ttu-id="d18c0-143">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d18c0-143">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="d18c0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d18c0-144">OUTPUTS</span></span>

### <span data-ttu-id="d18c0-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d18c0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="d18c0-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d18c0-146">NOTES</span></span>

## <span data-ttu-id="d18c0-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d18c0-147">RELATED LINKS</span></span>

[<span data-ttu-id="d18c0-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18c0-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d18c0-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18c0-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d18c0-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18c0-150">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


