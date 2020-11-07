---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 3431650296c29f06131f946910d1cbc3dc6e6bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762322"
---
# <span data-ttu-id="09d6a-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="09d6a-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="09d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="09d6a-103">Kapsayıcıyı yedek kasası ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="09d6a-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09d6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09d6a-104">SYNTAX</span></span>

### <span data-ttu-id="09d6a-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="09d6a-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d6a-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="09d6a-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d6a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="09d6a-108">**Register-AzureRmBackupContainer** cmdlet 'ı bir Azure Yedekleme Kasası ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="09d6a-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="09d6a-109">Azure yedekleme 'yi kullanarak yedeklemeyi yapılandırmak için, önce sunucunuzu veya sanal makinenizi bir yedek kasası ile kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="09d6a-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="09d6a-110">Bu cmdlet, bir altyapıyı belirtilen kasaya sahip bir hizmet (IaaS) sanal makinesi olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="09d6a-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="09d6a-111">Register işlemi, Azure sanal makinesini yedek kasası ile ilişkilendirir ve sanal makineyi yedekleme yaşam döngüsü aracılığıyla izler.</span><span class="sxs-lookup"><span data-stu-id="09d6a-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="09d6a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09d6a-112">EXAMPLES</span></span>

### <span data-ttu-id="09d6a-113">Örnek 1: yedekleme kasasına sanal makine kaydettirme</span><span class="sxs-lookup"><span data-stu-id="09d6a-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="09d6a-114">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="09d6a-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="09d6a-115">Komut $Vault değişkeninde kasayı depolar.</span><span class="sxs-lookup"><span data-stu-id="09d6a-115">The command stores the vault in the $Vault variable.</span></span>
<span data-ttu-id="09d6a-116">İkinci komut, Contoso03Vm adındaki sanal makineyi $Vault kasaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="09d6a-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="09d6a-117">Bu sanal makine, ContosoService27 adlı hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="09d6a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09d6a-118">PARAMETERS</span></span>

### <span data-ttu-id="09d6a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d6a-119">-DefaultProfile</span></span>
<span data-ttu-id="09d6a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="09d6a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09d6a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="09d6a-121">-Name</span></span>
<span data-ttu-id="09d6a-122">Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d6a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d6a-123">-ResourceGroupName</span></span>
<span data-ttu-id="09d6a-124">Sanal makine için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d6a-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="09d6a-125">-ServiceName</span></span>
<span data-ttu-id="09d6a-126">Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>
<span data-ttu-id="09d6a-127">Genellikle, bir bulut hizmeti adının soneki vardır. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="09d6a-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="09d6a-128">Bu parametreyi belirttiğinizde sonek eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="09d6a-128">Do not include the suffix when you specify this parameter.</span></span>
<span data-ttu-id="09d6a-129">Sanal makine hakkında bilgi edinmek için Get-AzureRMVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="09d6a-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="09d6a-130">Hizmet adı, sanal makine nesnesinin **DeploymentName** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d6a-131">-Kasa</span><span class="sxs-lookup"><span data-stu-id="09d6a-131">-Vault</span></span>
<span data-ttu-id="09d6a-132">Bu cmdlet 'in sanal makineyi kaydettiğinde Yedekleme Kasası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="09d6a-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="09d6a-133">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="09d6a-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d6a-134">CommonParameters</span></span>
<span data-ttu-id="09d6a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09d6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d6a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d6a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d6a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09d6a-137">INPUTS</span></span>

### <span data-ttu-id="09d6a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="09d6a-138">System.String</span></span>

### <span data-ttu-id="09d6a-139">Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="09d6a-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="09d6a-140">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="09d6a-140">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="09d6a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09d6a-141">OUTPUTS</span></span>

### <span data-ttu-id="09d6a-142">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="09d6a-142">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="09d6a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09d6a-143">NOTES</span></span>

## <span data-ttu-id="09d6a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09d6a-144">RELATED LINKS</span></span>

[<span data-ttu-id="09d6a-145">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="09d6a-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


