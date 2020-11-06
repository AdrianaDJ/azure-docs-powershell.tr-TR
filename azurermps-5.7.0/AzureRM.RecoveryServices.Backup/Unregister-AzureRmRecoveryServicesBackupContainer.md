---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591650"
---
# <span data-ttu-id="85c62-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="85c62-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="85c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c62-102">SYNOPSIS</span></span>
<span data-ttu-id="85c62-103">Bir Windows sunucusunun veya başka bir kapsayıcının kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="85c62-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85c62-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85c62-105">DESCRIPTION</span></span>
<span data-ttu-id="85c62-106">**Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet 'i, kasadan bir Windows sunucusunun veya diğer yedekleme kapsayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="85c62-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="85c62-107">Bu cmdlet, kasadaki bir kapsayıcıya yapılan başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85c62-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="85c62-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="85c62-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="85c62-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85c62-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="85c62-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85c62-110">EXAMPLES</span></span>

### <span data-ttu-id="85c62-111">Örnek 1: kasadan bir Windows sunucusunun kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="85c62-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="85c62-112">İlk komut, kasaya kaydedilen server01.contoso.com adındaki Windows kapsayıcısını alır ve $Cont değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="85c62-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="85c62-113">İkinci komut belirtilen Windows sunucusunun kaydını Azure yedekleme kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="85c62-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="85c62-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85c62-114">PARAMETERS</span></span>

### <span data-ttu-id="85c62-115">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="85c62-115">-Container</span></span>
<span data-ttu-id="85c62-116">Kaydı kaldırmak için bir yedekleme kapsayıcısı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="85c62-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="85c62-117">**Backupcontainer** nesnesi almak için Get-AzureRmRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="85c62-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c62-118">-DefaultProfile</span></span>
<span data-ttu-id="85c62-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85c62-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c62-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="85c62-120">-PassThru</span></span>
<span data-ttu-id="85c62-121">Silinecek kapsayıcıyı döndürün.</span><span class="sxs-lookup"><span data-stu-id="85c62-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="85c62-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="85c62-122">-Confirm</span></span>
<span data-ttu-id="85c62-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85c62-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c62-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c62-124">-WhatIf</span></span>
<span data-ttu-id="85c62-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85c62-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85c62-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85c62-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c62-127">CommonParameters</span></span>
<span data-ttu-id="85c62-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85c62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c62-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c62-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c62-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85c62-130">INPUTS</span></span>

### <span data-ttu-id="85c62-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="85c62-131">None</span></span>
<span data-ttu-id="85c62-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="85c62-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85c62-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85c62-133">OUTPUTS</span></span>

## <span data-ttu-id="85c62-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85c62-134">NOTES</span></span>

## <span data-ttu-id="85c62-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85c62-135">RELATED LINKS</span></span>

[<span data-ttu-id="85c62-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="85c62-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


