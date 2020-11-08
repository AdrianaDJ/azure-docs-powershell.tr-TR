---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105278"
---
# <span data-ttu-id="1cd9f-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="1cd9f-101">Get-AzsDisk</span></span>

## <span data-ttu-id="1cd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd9f-103">Diski döndürür.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-103">Returns the disk.</span></span>

## <span data-ttu-id="1cd9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cd9f-104">SYNTAX</span></span>

### <span data-ttu-id="1cd9f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1cd9f-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cd9f-106">Al</span><span class="sxs-lookup"><span data-stu-id="1cd9f-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cd9f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1cd9f-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1cd9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cd9f-108">DESCRIPTION</span></span>
<span data-ttu-id="1cd9f-109">Diski döndürür.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-109">Returns the disk.</span></span>

## <span data-ttu-id="1cd9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cd9f-110">EXAMPLES</span></span>

### <span data-ttu-id="1cd9f-111">Örnek 1: tüm diskleri Al</span><span class="sxs-lookup"><span data-stu-id="1cd9f-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="1cd9f-112">Parametresiz, `Get-AzsDisk` tüm diskleri listeler.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="1cd9f-113">Örnek 2: ada göre disk alma</span><span class="sxs-lookup"><span data-stu-id="1cd9f-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="1cd9f-114">Bir diski `Name` alacak şekilde belirtin.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="1cd9f-115">Örnek 3: belirtilen sayıda disk edinme</span><span class="sxs-lookup"><span data-stu-id="1cd9f-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="1cd9f-116">`Count`Belirli sayıda diski almak için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="1cd9f-117">Örnek 4: belirli konumdaki tüm diskleri alma</span><span class="sxs-lookup"><span data-stu-id="1cd9f-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="1cd9f-118">`ScaleUnit` `VolumeLabel` Belirli konumdaki tüm diskleri listelemek için veya parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="1cd9f-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="1cd9f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cd9f-119">PARAMETERS</span></span>

### <span data-ttu-id="1cd9f-120">-Sayı</span><span class="sxs-lookup"><span data-stu-id="1cd9f-120">-Count</span></span>
<span data-ttu-id="1cd9f-121">Döndürülecek en fazla disk sayısı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd9f-122">-DefaultProfile</span></span>
<span data-ttu-id="1cd9f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cd9f-124">-InputObject</span></span>
<span data-ttu-id="1cd9f-125">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="1cd9f-126">-Location</span></span>
<span data-ttu-id="1cd9f-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cd9f-128">-Name</span></span>
<span data-ttu-id="1cd9f-129">Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1cd9f-130">-ScaleUnit</span></span>
<span data-ttu-id="1cd9f-131">Kaynağın ait olduğu ölçeklendirme birimi.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-131">The scale unit which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="1cd9f-132">-SharePath</span></span>
<span data-ttu-id="1cd9f-133">Kaynağın ait olduğu paylaşım.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-133">The share which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-134">-Başlangıç</span><span class="sxs-lookup"><span data-stu-id="1cd9f-134">-Start</span></span>
<span data-ttu-id="1cd9f-135">Sorgudaki disklerin başlangıç dizini.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-136">-Durum</span><span class="sxs-lookup"><span data-stu-id="1cd9f-136">-Status</span></span>
<span data-ttu-id="1cd9f-137">Disk durumunun parametreleri.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-137">The parameters of disk state.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1cd9f-138">-SubscriptionId</span></span>
<span data-ttu-id="1cd9f-139">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cd9f-140">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-141">-Usersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="1cd9f-141">-UserSubscriptionId</span></span>
<span data-ttu-id="1cd9f-142">Kaynağın ait olduğu kullanıcı aboneliği kimliği.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-142">User Subscription Id which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-143">-Birimetiketi</span><span class="sxs-lookup"><span data-stu-id="1cd9f-143">-VolumeLabel</span></span>
<span data-ttu-id="1cd9f-144">Kaynağın ait olduğu birimin Birim etiketi.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-144">The volume label of the volume which the resource belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1cd9f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd9f-145">CommonParameters</span></span>
<span data-ttu-id="1cd9f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd9f-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd9f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cd9f-148">INPUTS</span></span>

### <span data-ttu-id="1cd9f-149">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. ıuteadminıdentity</span><span class="sxs-lookup"><span data-stu-id="1cd9f-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="1cd9f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cd9f-150">OUTPUTS</span></span>

### <span data-ttu-id="1cd9f-151">Microsoft. Azure. PowerShell. cmdlet. ComputeAdmin. modeller. Api20180730Preview. ıdisk</span><span class="sxs-lookup"><span data-stu-id="1cd9f-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="1cd9f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cd9f-152">NOTES</span></span>

<span data-ttu-id="1cd9f-153">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cd9f-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1cd9f-155">INPUTOBJECT <IComputeAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1cd9f-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cd9f-156">`[DiskId <String>]`: Kimlik olarak disk Guid 'si.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="1cd9f-157">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1cd9f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cd9f-158">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1cd9f-159">`[MigrationId <String>]`: Geçiş işi GUID adı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="1cd9f-160">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="1cd9f-161">`[Publisher <String>]`: Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="1cd9f-162">`[QuotaName <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1cd9f-163">`[Sku <String>]`: SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="1cd9f-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1cd9f-165">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1cd9f-166">`[Type <String>]`: Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="1cd9f-167">`[Version <String>]`: Kaynağın sürümü.</span><span class="sxs-lookup"><span data-stu-id="1cd9f-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="1cd9f-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cd9f-168">RELATED LINKS</span></span>

