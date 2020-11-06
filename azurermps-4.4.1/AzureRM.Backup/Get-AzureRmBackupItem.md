---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588000"
---
# <span data-ttu-id="ce807-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="ce807-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="ce807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce807-102">SYNOPSIS</span></span>
<span data-ttu-id="ce807-103">Yedeklemede bir kapsayıcının altındaki öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="ce807-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce807-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce807-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce807-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce807-105">DESCRIPTION</span></span>
<span data-ttu-id="ce807-106">**Get-Azurermbackupıtem** cmdlet 'ı Azure Backup 'daki bir kapsayıcıdaki öğeleri ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ce807-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="ce807-107">Enable-AzureRmBackupProtection cmdlet 'ini kullanarak öğeleri koruma için etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ce807-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="ce807-108">Yedek kasaya kaydedilen bir kapsayıcı, korunabilir bir veya birden çok öğe içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ce807-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="ce807-109">Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="ce807-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="ce807-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce807-110">EXAMPLES</span></span>

### <span data-ttu-id="ce807-111">Örnek 1: kapsayıcıdaki öğeleri alma</span><span class="sxs-lookup"><span data-stu-id="ce807-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="ce807-112">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="ce807-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="ce807-113">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ce807-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ce807-114">İkinci komut, **Get-AzureRmBackupContainer** cmdlet 'ini kullanarak $Vault kasada belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="ce807-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="ce807-115">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ce807-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="ce807-116">Son komutu $Container kapsayıcısındaki yedekleme öğesini alır.</span><span class="sxs-lookup"><span data-stu-id="ce807-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="ce807-117">Örnek 2: öğenin tüm özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ce807-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="ce807-118">Bu komut, $Container kapsayıcısındaki yedekleme öğesini alır ve Select-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="ce807-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="ce807-119">Bu cmdlet yedek öğesinin tüm özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce807-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="ce807-120">Daha fazla bilgi için yazın `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="ce807-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="ce807-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce807-121">PARAMETERS</span></span>

### <span data-ttu-id="ce807-122">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ce807-122">-Container</span></span>
<span data-ttu-id="ce807-123">Bu cmdlet 'in yedekleme öğelerini aldığı kapsayıcı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce807-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="ce807-124">**Azurermbackupcontainer** almak için Get-AzureRmBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ce807-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce807-125">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="ce807-125">-ProtectionStatus</span></span>
<span data-ttu-id="ce807-126">Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce807-126">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="ce807-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ce807-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce807-128">Korunamaz</span><span class="sxs-lookup"><span data-stu-id="ce807-128">Protected</span></span> 
- <span data-ttu-id="ce807-129">Bilgilerinizin</span><span class="sxs-lookup"><span data-stu-id="ce807-129">Protecting</span></span>  
- <span data-ttu-id="ce807-130">NotProtected</span><span class="sxs-lookup"><span data-stu-id="ce807-130">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce807-131">-Durum</span><span class="sxs-lookup"><span data-stu-id="ce807-131">-Status</span></span>
<span data-ttu-id="ce807-132">Öğenin yedekleme durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce807-132">Specifies the backup status for an item.</span></span>
<span data-ttu-id="ce807-133">Bu parametre için kabul edilebilir değerler: ırpending, protected, ProtectionError ve Protectiondurdurdu.</span><span class="sxs-lookup"><span data-stu-id="ce807-133">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="ce807-134">*Protectionstatus* parametresinde değer varsa, öğeleri filtrelemek için *durum* parametre değerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce807-134">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce807-135">-Tür</span><span class="sxs-lookup"><span data-stu-id="ce807-135">-Type</span></span>
<span data-ttu-id="ce807-136">Bu cmdlet 'in aldığı öğenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce807-136">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="ce807-137">Şu anda desteklenen tek değer AzureVM.</span><span class="sxs-lookup"><span data-stu-id="ce807-137">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce807-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce807-138">-DefaultProfile</span></span>
<span data-ttu-id="ce807-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce807-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce807-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce807-140">CommonParameters</span></span>
<span data-ttu-id="ce807-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce807-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce807-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce807-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce807-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce807-143">INPUTS</span></span>

### <span data-ttu-id="ce807-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ce807-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="ce807-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce807-145">OUTPUTS</span></span>

### <span data-ttu-id="ce807-146">Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ce807-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="ce807-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce807-147">NOTES</span></span>

## <span data-ttu-id="ce807-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce807-148">RELATED LINKS</span></span>

[<span data-ttu-id="ce807-149">Backup-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ce807-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="ce807-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ce807-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="ce807-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ce807-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="ce807-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ce807-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="ce807-153">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ce807-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ce807-154">Restore-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ce807-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


