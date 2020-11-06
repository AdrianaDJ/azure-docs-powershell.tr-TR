---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587483"
---
# <span data-ttu-id="821c2-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="821c2-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="821c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821c2-102">SYNOPSIS</span></span>
<span data-ttu-id="821c2-103">Bir kasadan yedek koruma ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="821c2-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="821c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="821c2-104">SYNTAX</span></span>

### <span data-ttu-id="821c2-105">PolicyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="821c2-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="821c2-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="821c2-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="821c2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="821c2-107">DESCRIPTION</span></span>
<span data-ttu-id="821c2-108">**Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet 'inin yedekleme ilkelerini siler.</span><span class="sxs-lookup"><span data-stu-id="821c2-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="821c2-109">Yedekleme koruma ilkesini silebilmeniz için, ilkenin ilişkili yedekleme öğeleri olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="821c2-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="821c2-110">İlkeyi silmeden önce, her ilişkili öğenin başka bir ilkeyle ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="821c2-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="821c2-111">Başka bir ilkeyi yedekleme öğesiyle ilişkilendirmek için Enable-AzureRmRecoveryServicesBackupProtection cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="821c2-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="821c2-112">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="821c2-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="821c2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="821c2-113">EXAMPLES</span></span>

### <span data-ttu-id="821c2-114">Örnek 1: ilkeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="821c2-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="821c2-115">İlk komut NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="821c2-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="821c2-116">İkinci komut $Pol ilke nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="821c2-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="821c2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="821c2-117">PARAMETERS</span></span>

### <span data-ttu-id="821c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821c2-118">-DefaultProfile</span></span>
<span data-ttu-id="821c2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="821c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="821c2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="821c2-120">-Force</span></span>
<span data-ttu-id="821c2-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="821c2-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="821c2-122">-Name</span></span>
<span data-ttu-id="821c2-123">Kaldırılacak yedekleme koruması ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="821c2-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="821c2-124">-PassThru</span></span>
<span data-ttu-id="821c2-125">Silinecek ilkeyi döndür.</span><span class="sxs-lookup"><span data-stu-id="821c2-125">Return the policy to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-126">-İlke</span><span class="sxs-lookup"><span data-stu-id="821c2-126">-Policy</span></span>
<span data-ttu-id="821c2-127">Kaldırılacak yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="821c2-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="821c2-128">**Yedeklemeilkesi** nesnesi almak için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="821c2-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="821c2-129">-Confirm</span></span>
<span data-ttu-id="821c2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="821c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821c2-131">-WhatIf</span></span>
<span data-ttu-id="821c2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="821c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="821c2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="821c2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821c2-134">CommonParameters</span></span>
<span data-ttu-id="821c2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="821c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821c2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821c2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="821c2-137">INPUTS</span></span>

### <span data-ttu-id="821c2-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="821c2-138">PolicyBase</span></span>
<span data-ttu-id="821c2-139">Parametre ' Ilke ', ardışık düzenin ' PolicyBase ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="821c2-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="821c2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="821c2-140">OUTPUTS</span></span>

## <span data-ttu-id="821c2-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="821c2-141">NOTES</span></span>

## <span data-ttu-id="821c2-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="821c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="821c2-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="821c2-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="821c2-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="821c2-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="821c2-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="821c2-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


