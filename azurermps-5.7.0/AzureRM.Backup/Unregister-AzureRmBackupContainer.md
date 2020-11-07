---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765109"
---
# <span data-ttu-id="59fee-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fee-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="59fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fee-102">SYNOPSIS</span></span>
<span data-ttu-id="59fee-103">Yedek kasasından kapsayıcıyı silme.</span><span class="sxs-lookup"><span data-stu-id="59fee-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59fee-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59fee-105">DESCRIPTION</span></span>
<span data-ttu-id="59fee-106">**Unregister-AzureRmBackupContainer** cmdlet 'i, bir Azure yedekleme kasasından Windows sunucusunun veya Azure sanal makinesinin kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="59fee-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="59fee-107">Bu cmdlet, yedek kasasından gelen başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59fee-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="59fee-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="59fee-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="59fee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59fee-109">EXAMPLES</span></span>

### <span data-ttu-id="59fee-110">Örnek 1: Windows sunucusunun kaydını silme</span><span class="sxs-lookup"><span data-stu-id="59fee-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="59fee-111">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="59fee-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="59fee-112">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59fee-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="59fee-113">İkinci komut, Get-AzureRmBackupContainer cmdlet 'ini kullanarak $Vault belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="59fee-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="59fee-114">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59fee-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="59fee-115">Son komutu, belirtilen Windows sunucusunun Azure yedekleme kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="59fee-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="59fee-116">Örnek 2: onaysız bir Windows sunucusunun kaydını silme</span><span class="sxs-lookup"><span data-stu-id="59fee-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="59fee-117">Bu komut, ilk örnekte olduğu gibi, belirtilen Windows Server 'ın Azure yedekleme kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="59fee-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="59fee-118">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59fee-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="59fee-119">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="59fee-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="59fee-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59fee-120">PARAMETERS</span></span>

### <span data-ttu-id="59fee-121">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="59fee-121">-Container</span></span>
<span data-ttu-id="59fee-122">Bu cmdlet 'in kaydını belirttiği Windows Server veya Azure sanal makinesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59fee-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="59fee-123">**Azurermbackupcontainer** almak için Get-AzureRmBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="59fee-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fee-124">-DefaultProfile</span></span>
<span data-ttu-id="59fee-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59fee-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59fee-126">-Force</span><span class="sxs-lookup"><span data-stu-id="59fee-126">-Force</span></span>
<span data-ttu-id="59fee-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="59fee-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="59fee-128">Bu parametre yalnızca Windows türündeki **AzureBackupContainer** nesnelerinde ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="59fee-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fee-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="59fee-129">-Confirm</span></span>
<span data-ttu-id="59fee-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59fee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fee-131">-WhatIf</span></span>
<span data-ttu-id="59fee-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59fee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fee-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59fee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fee-134">CommonParameters</span></span>
<span data-ttu-id="59fee-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59fee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fee-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fee-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59fee-137">INPUTS</span></span>

### <span data-ttu-id="59fee-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fee-138">AzureBackupContainer</span></span>

## <span data-ttu-id="59fee-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59fee-139">OUTPUTS</span></span>

### <span data-ttu-id="59fee-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="59fee-140">AzureBackupJob</span></span>
<span data-ttu-id="59fee-141">Kapsayıcı türü Windows Server olduğunda, bu cmdlet $Null döndürür.</span><span class="sxs-lookup"><span data-stu-id="59fee-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="59fee-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59fee-142">NOTES</span></span>
* <span data-ttu-id="59fee-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59fee-143">None</span></span>

## <span data-ttu-id="59fee-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59fee-144">RELATED LINKS</span></span>

[<span data-ttu-id="59fee-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fee-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="59fee-146">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="59fee-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="59fee-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="59fee-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


