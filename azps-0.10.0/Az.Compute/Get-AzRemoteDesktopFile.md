---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937046"
---
# <span data-ttu-id="ed419-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="ed419-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="ed419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed419-102">SYNOPSIS</span></span>
<span data-ttu-id="ed419-103">Bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="ed419-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="ed419-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed419-104">SYNTAX</span></span>

### <span data-ttu-id="ed419-105">İndirin</span><span class="sxs-lookup"><span data-stu-id="ed419-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed419-106">Başlatılması</span><span class="sxs-lookup"><span data-stu-id="ed419-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed419-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed419-107">DESCRIPTION</span></span>
<span data-ttu-id="ed419-108">**Get-AzRemoteDesktopFile** cmdlet 'ı bir Uzak Masaüstü Protokolü (. rdp) dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="ed419-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="ed419-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed419-109">EXAMPLES</span></span>

### <span data-ttu-id="ed419-110">Örnek 1: uzak masaüstü dosyası alma</span><span class="sxs-lookup"><span data-stu-id="ed419-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="ed419-111">Bu komut, VirtualMachine07 adındaki sanal makine için Uzak Masaüstü dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="ed419-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ed419-112">Komut, sonucu D:\remotedesktopfile07.rdpadındaki dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="ed419-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="ed419-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed419-113">PARAMETERS</span></span>

### <span data-ttu-id="ed419-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed419-114">-DefaultProfile</span></span>
<span data-ttu-id="ed419-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed419-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed419-116">-Başlat</span><span class="sxs-lookup"><span data-stu-id="ed419-116">-Launch</span></span>
<span data-ttu-id="ed419-117">Bu cmdlet. rdp dosyasını aldıktan sonra uzak masaüstünü başlatıyor.</span><span class="sxs-lookup"><span data-stu-id="ed419-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed419-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ed419-118">-LocalPath</span></span>
<span data-ttu-id="ed419-119">Bu cmdlet. rdp dosyasını depolayan yerel tam yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed419-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed419-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed419-120">-Name</span></span>
<span data-ttu-id="ed419-121">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed419-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed419-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed419-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed419-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed419-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed419-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed419-124">CommonParameters</span></span>
<span data-ttu-id="ed419-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed419-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed419-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed419-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed419-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed419-127">INPUTS</span></span>

### <span data-ttu-id="ed419-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed419-128">None</span></span>
<span data-ttu-id="ed419-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ed419-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed419-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed419-130">OUTPUTS</span></span>

## <span data-ttu-id="ed419-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed419-131">NOTES</span></span>

## <span data-ttu-id="ed419-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed419-132">RELATED LINKS</span></span>

