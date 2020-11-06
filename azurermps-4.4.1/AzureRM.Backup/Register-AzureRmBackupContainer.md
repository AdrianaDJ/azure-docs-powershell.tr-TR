---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591164"
---
# <span data-ttu-id="96252-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="96252-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="96252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96252-102">SYNOPSIS</span></span>
<span data-ttu-id="96252-103">Kapsayıcıyı yedek kasası ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="96252-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96252-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96252-104">SYNTAX</span></span>

### <span data-ttu-id="96252-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="96252-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96252-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="96252-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96252-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="96252-107">DESCRIPTION</span></span>
<span data-ttu-id="96252-108">**Register-AzureRmBackupContainer** cmdlet 'ı bir Azure Yedekleme Kasası ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="96252-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="96252-109">Azure yedekleme 'yi kullanarak yedeklemeyi yapılandırmak için, önce sunucunuzu veya sanal makinenizi bir yedek kasası ile kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="96252-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="96252-110">Bu cmdlet, bir altyapıyı belirtilen kasaya sahip bir hizmet (IaaS) sanal makinesi olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="96252-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="96252-111">Register işlemi, Azure sanal makinesini yedek kasası ile ilişkilendirir ve sanal makineyi yedekleme yaşam döngüsü aracılığıyla izler.</span><span class="sxs-lookup"><span data-stu-id="96252-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="96252-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96252-112">EXAMPLES</span></span>

### <span data-ttu-id="96252-113">Örnek 1: yedekleme kasasına sanal makine kaydettirme</span><span class="sxs-lookup"><span data-stu-id="96252-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="96252-114">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="96252-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="96252-115">Komut $Vault değişkeninde kasayı depolar.</span><span class="sxs-lookup"><span data-stu-id="96252-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="96252-116">İkinci komut, Contoso03Vm adındaki sanal makineyi $Vault kasaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="96252-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="96252-117">Bu sanal makine, ContosoService27 adlı hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="96252-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="96252-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96252-118">PARAMETERS</span></span>

### <span data-ttu-id="96252-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="96252-119">-Name</span></span>
<span data-ttu-id="96252-120">Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96252-120">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="96252-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96252-121">-ResourceGroupName</span></span>
<span data-ttu-id="96252-122">Sanal makine için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96252-122">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="96252-123">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="96252-123">-ServiceName</span></span>
<span data-ttu-id="96252-124">Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96252-124">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="96252-125">Genellikle, bir bulut hizmeti adının soneki vardır. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="96252-125">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="96252-126">Bu parametreyi belirttiğinizde sonek eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="96252-126">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="96252-127">Sanal makine hakkında bilgi edinmek için Get-AzureRMVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="96252-127">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="96252-128">Hizmet adı, sanal makine nesnesinin **DeploymentName** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="96252-128">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

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

### <span data-ttu-id="96252-129">-Kasa</span><span class="sxs-lookup"><span data-stu-id="96252-129">-Vault</span></span>
<span data-ttu-id="96252-130">Bu cmdlet 'in sanal makineyi kaydettiğinde Yedekleme Kasası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="96252-130">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="96252-131">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="96252-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="96252-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96252-132">-DefaultProfile</span></span>
<span data-ttu-id="96252-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96252-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96252-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96252-134">CommonParameters</span></span>
<span data-ttu-id="96252-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96252-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96252-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96252-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96252-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96252-137">INPUTS</span></span>

### <span data-ttu-id="96252-138">Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="96252-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="96252-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96252-139">OUTPUTS</span></span>

### <span data-ttu-id="96252-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="96252-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="96252-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96252-141">NOTES</span></span>

## <span data-ttu-id="96252-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96252-142">RELATED LINKS</span></span>

[<span data-ttu-id="96252-143">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="96252-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


