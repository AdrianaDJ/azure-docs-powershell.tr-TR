---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277679"
---
# <span data-ttu-id="460b7-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="460b7-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="460b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="460b7-102">SYNOPSIS</span></span>
<span data-ttu-id="460b7-103">Yedekleme yönetiminin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="460b7-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="460b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="460b7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="460b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="460b7-105">DESCRIPTION</span></span>
<span data-ttu-id="460b7-106">**Set-AzRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme depolama özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="460b7-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="460b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="460b7-107">EXAMPLES</span></span>

### <span data-ttu-id="460b7-108">Örnek 1: kasa için Jeo uzamsal depolama ayarlama</span><span class="sxs-lookup"><span data-stu-id="460b7-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="460b7-109">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="460b7-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="460b7-110">İkinci komut $Vault 01 yedek depolama fazlaesini Geoyedekli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="460b7-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="460b7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="460b7-111">PARAMETERS</span></span>

### <span data-ttu-id="460b7-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="460b7-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="460b7-113">Yedek depolama artıklık türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="460b7-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="460b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460b7-114">-DefaultProfile</span></span>
<span data-ttu-id="460b7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="460b7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="460b7-116">-Kasa</span><span class="sxs-lookup"><span data-stu-id="460b7-116">-Vault</span></span>
<span data-ttu-id="460b7-117">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="460b7-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="460b7-118">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="460b7-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="460b7-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="460b7-119">-Confirm</span></span>
<span data-ttu-id="460b7-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="460b7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460b7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460b7-121">-WhatIf</span></span>
<span data-ttu-id="460b7-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="460b7-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="460b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460b7-123">CommonParameters</span></span>
<span data-ttu-id="460b7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="460b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460b7-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="460b7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460b7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="460b7-126">INPUTS</span></span>

### <span data-ttu-id="460b7-127">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="460b7-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="460b7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="460b7-128">OUTPUTS</span></span>

### <span data-ttu-id="460b7-129">System. void</span><span class="sxs-lookup"><span data-stu-id="460b7-129">System.Void</span></span>

## <span data-ttu-id="460b7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="460b7-130">NOTES</span></span>

## <span data-ttu-id="460b7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="460b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="460b7-132">Get-Azrecoveryservicesbackupözelliği</span><span class="sxs-lookup"><span data-stu-id="460b7-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="460b7-133">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="460b7-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


