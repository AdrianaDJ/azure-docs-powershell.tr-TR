---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105511"
---
# <span data-ttu-id="20ee4-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="20ee4-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="20ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="20ee4-103">Sanal StorSimple cihazı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20ee4-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="20ee4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20ee4-104">SYNTAX</span></span>

### <span data-ttu-id="20ee4-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20ee4-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20ee4-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20ee4-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20ee4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="20ee4-108">**New-AzureStorSimpleVirtualDevice** cmdlet 'ı sanal StorSimple cihazı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20ee4-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="20ee4-109">Cihaz için bir cihaz adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="20ee4-109">Specify a device name for the device.</span></span>
<span data-ttu-id="20ee4-110">Aynı abonelikteki sanal ağın sanal ağ ve alt ağ ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="20ee4-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="20ee4-111">Coğrafi olarak, StorSimple kaynağının oluşturulduğu coğrafi değer eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="20ee4-112">Bu sanal cihaz için var olan bir depolama hesabını kullanmak için, adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="20ee4-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="20ee4-113">Bu sanal cihaz için yeni bir depolama hesabı oluşturmak için hem *storageAccountName* hem de *createnewstorageaccount* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="20ee4-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="20ee4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20ee4-114">EXAMPLES</span></span>

### <span data-ttu-id="20ee4-115">Örnek 1: yeni bir hesap ve var olan bir ağ ile sanal cihaz oluşturma</span><span class="sxs-lookup"><span data-stu-id="20ee4-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="20ee4-116">Bu komut yeni bir depolama hesabı ve var olan sanal ağ kullanan bir sanal cihaz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20ee4-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="20ee4-117">Örnek 2: var olan bir hesap ve sanal ağ ile sanal cihaz oluşturma</span><span class="sxs-lookup"><span data-stu-id="20ee4-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="20ee4-118">Bu komut, var olan bir depolama hesabını ve var olan sanal ağı kullanan bir sanal cihaz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20ee4-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="20ee4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20ee4-119">PARAMETERS</span></span>

### <span data-ttu-id="20ee4-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20ee4-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="20ee4-121">Bu cmdlet 'in yeni bir depolama hesabı oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="20ee4-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="20ee4-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="20ee4-123">-Profile</span></span>
<span data-ttu-id="20ee4-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20ee4-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="20ee4-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20ee4-126">-StorageAccountName</span></span>
<span data-ttu-id="20ee4-127">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="20ee4-128">-SubNetName</span></span>
<span data-ttu-id="20ee4-129">Sanal alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-129">Specifies the name of a virtual subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-130">-Sanalaygıtadı</span><span class="sxs-lookup"><span data-stu-id="20ee4-130">-VirtualDeviceName</span></span>
<span data-ttu-id="20ee4-131">Sanal cihaz için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="20ee4-132">-VirtualNetworkName</span></span>
<span data-ttu-id="20ee4-133">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20ee4-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ee4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ee4-134">CommonParameters</span></span>
<span data-ttu-id="20ee4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20ee4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ee4-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ee4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ee4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20ee4-137">INPUTS</span></span>

## <span data-ttu-id="20ee4-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20ee4-138">OUTPUTS</span></span>

### <span data-ttu-id="20ee4-139">Dizisi</span><span class="sxs-lookup"><span data-stu-id="20ee4-139">String</span></span>
<span data-ttu-id="20ee4-140">Bu cmdlet, sanal cihazı oluşturan işin KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="20ee4-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="20ee4-141">Get-AzureStorSimpleJob cmdlet 'ini kullanarak ilerlemeyi izlemek için bu KIMLIĞI kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20ee4-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="20ee4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20ee4-142">NOTES</span></span>

## <span data-ttu-id="20ee4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20ee4-143">RELATED LINKS</span></span>

[<span data-ttu-id="20ee4-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="20ee4-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="20ee4-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="20ee4-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


